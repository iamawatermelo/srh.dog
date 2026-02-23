<script module lang="ts">
    export interface ContractTemplateInput {
        what: string;
        id: string;
        providingEntity: string;
        lastUpdated: Date;
        contactName: string;
        contactUri: string;
        changeNotifications: string;

        // Restrictions
        minimumAge: number;
        extraSections: Array<{
            header: string;
            body: Snippet;
        }>;

        // Privacy
        collectedInformation: Array<{
            data: string;
            why: string;
        }>;
        subprocessors: Array<{
            who: string;
            dpa: string;
        }>;
        dataRetention: string;
        dataDeletion?: {
            method: string;
            uri: string;
        };
        dataStorage: string;

        // AI
        genai: boolean;
        genaiTraining: boolean;
        genaiUses: Array<string>;
    }
</script>

<script lang="ts">
    import type { Snippet } from 'svelte';

    const {
        template
    }: {
        template: ContractTemplateInput;
    } = $props();
    let accessible = $state(false);
    let lessLegalese = $state(false);

    const titleToId = (text: string) => {
        return text
            .toLowerCase()
            .trim()
            .normalize('NFD')
            .replace(/[\u0300-\u036f]/g, '')
            .replace(/[\s\W|_]+/g, '-')
            .replace(/^-+|-+$/g, '');
    };
</script>

<svelte:head>
    <title>Terms of use and privacy policy for {template.what} | {template.id}</title>
</svelte:head>

<main class:accessible>
    <h1>Terms of use and privacy policy for {template.what}</h1>

    <button onclick={() => (accessible = !accessible)}>Use {accessible ? 'website font' : 'system font'}</button>

    <p>
        By interacting with {template.what} (referred to as the "service") you agree to the following terms of use and privacy
        policy (called the "terms"). If you do not agree to these terms you must not use the service.
    </p>

    <p>
        This service is provided by {template.providingEntity} (referred to as "we", "us" or "our"). This document forms
        a contract between you and {template.providingEntity}.
    </p>
    
    <p>
        These terms will be governed and disputes will be resolved under the laws of England and Wales.
    </p>

    <h2 id="notice-summary">Notice summary</h2>

    <p>
        This is a purely informative summary of these terms. This section does not constitute a legally binding portion
        of these terms.
    </p>

    <table>
        <thead>
            <tr>
                <th scope="col">Term</th>
                <th scope="col">Type</th>
                <th scope="col">Value</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th scope="row">Document identifier</th>
                <td class="type">entity</td>
                <td>{template.id}</td>
            </tr>
            <tr>
                <th scope="row">Last updated</th>
                <td class="type">date</td>
                <td>{template.lastUpdated.toLocaleDateString('en-GB', { dateStyle: 'medium' })}</td>
            </tr>
            <tr>
                <th scope="row">Notification of changes</th>
                <td class="type">string</td>
                <td>{template.changeNotifications}</td>
            </tr>

            <!-- Restrictions -->
            <tr>
                <th scope="row">Minimum age to use service</th>
                <td class="type">integer</td>
                <td>{template.minimumAge}</td>
            </tr>

            <!-- Privacy -->
            <tr>
                <th scope="row">Collected information</th>
                <td class="type">array&lt;string&gt;</td>
                <td>
                    <ol>
                        {#each template.collectedInformation as data (data.data)}
                            <li>{data.data}</li>
                        {/each}
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">Data subprocessors</th>
                <td class="type">array&lt;link&gt;</td>
                <td>
                    <ol>
                        {#each template.subprocessors as subprocessor (subprocessor.who)}
                            <li><a href={subprocessor.dpa}>{subprocessor.who}</a></li>
                        {/each}
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">Data storage</th>
                <td class="type">enumeration</td>
                <td>{template.dataStorage}</td>
            </tr>
            <tr>
                <th scope="row">Data retention</th>
                <td class="type">enumeration</td>
                <td>{template.dataRetention}</td>
            </tr>
            <tr>
                <th scope="row">Data deletion</th>
                <td class="type">enumeration</td>
                <td>
                    {#if template.dataDeletion}
                        <a href={template.dataDeletion.uri}>{template.dataDeletion.method}</a>
                    {:else}
                        Manual, by contact
                    {/if}
                </td>
            </tr>

            <!-- AI -->
            <tr>
                <th scope="row">AI processing</th>
                <td class="type">enumeration</td>
                <td>
                    {#if template.genai}
                        This service processes your data with Generative AI
                    {:else}
                        This service does not process your data with Generative AI
                    {/if}
                </td>
            </tr>
            {#if template.genai}
                <tr>
                    <th scope="row">AI training</th>
                    <td class="type">enumeration</td>
                    <td
                        >{template.genaiTraining
                            ? 'This service uses your data to train Generative AI models'
                            : 'This service does not use your data to train Generative AI models'}</td>
                </tr>
            {/if}

            <tr>
                <th scope="row">Point of contact</th>
                <td class="type">email</td>
                <td><a href={template.contactUri}>{template.contactName}</a></td>
            </tr>
        </tbody>
    </table>

    <h2 id="contents">Table of contents</h2>

    <ol>
        <li><a href="#notice-summary">Notice summary</a></li>
        <li><a href="#contents">Table of contents</a></li>
        <li>
            <a href="#terms-of-use">Terms of use</a>
            <ol>
                <li><a href="#changes">Changes to these terms of use</a></li>
                {#each template.extraSections as section (section.header)}
                    <li><a href={`#ext-${titleToId(section.header)}`}>{section.header}</a></li>
                {/each}
                <li><a href="#minimum-age">Minimum age</a></li>
                <li><a href="#liability">Limitation of liability</a></li>
                <li><a href="#severability">Severability</a></li>
                <li><a href="#contact">Contact</a></li>
            </ol>
        </li>
        <li>
            <a href="#privacy-policy">Privacy policy</a>
            <ol>
                <li><a href="#data-collected">What information do we collect and why?</a></li>
                {#if template.genai}
                    <li><a href="#genai">Generative AI</a></li>
                {/if}
                <li><a href="#dpa">Who processes my data?</a></li>
                <li><a href="#data-storage">How is my data stored?</a></li>
                <li><a href="#data-deletion">How do I delete my data?</a></li>
                <li><a href="#data-rights">What are my rights as a data subject?</a></li>
                <li><a href="#data-contact">Who do I contact regarding my personal data?</a></li>
            </ol>
        </li>
    </ol>
    
    <h2 id="terms-of-use">Terms of use</h2>

    <p>This section details the terms under which the service is provided to you.</p>

    <h3 id="changes">Changes to these terms of use</h3>
    
    <p>
        You will be notified of changes to these terms of use {template.changeNotifications}. Continued use of the service constitutes acceptance of any new terms. If you do not agree with any new terms, you must stop using the service.
    </p>
    
    {#each template.extraSections as section (section.header)}
        <h3 id={`ext-${titleToId(section.header)}`}>{section.header}</h3>
        {@render section.body()}
    {/each}

    <h3 id="minimum-age">Minimum age</h3>

    <p>
        The minimum age to use this service is {template.minimumAge} years old. People under {template.minimumAge} years
        old may not use the service. Users agree that they are at least {template.minimumAge} years old when using the service.
        Access will be restricted to users under 16.
    </p>

    <h3 id="liability">Limitation of liability</h3>
    
    {#snippet liability(uppercase: boolean)}
        {@const liabilityText = `The service is provided on an as-is basis. Except in the case of fraud, death or personal injury caused by our negligence, gross negligence or wilful misconduct, to the extent permitted by UK law, you'll indemnify and hold harmless ${template.providingEntity} and its affiliates. This indemnity covers any liability and expense arising from claims, losses, damages, judgements, fines, litigation costs and legal fees, except to the extent a liability or expense is caused by our breach, negligence or wilful misconduct.`}
        
        <strong class="pre-warning">You should read this section carefully.</strong>
        
        <div class="liability-warning">
            <div class="symbol" role="presentation">⚠</div>
            <p class="text">
                {#if uppercase}
                    {liabilityText}
                {:else}
                    {liabilityText.toUpperCase()}
                {/if}
            </p>
        </div>
        
        <style>
            .pre-warning {
                font-family: "Iosevka Expanded", system-ui;
                font-weight: normal;
                font-size: 1rem;
                background: var(--color);
                color: var(--inverse);
                padding: 0.25em 0.5em;
                
                display: block;
                text-align: center;
                
                &::selection {
                    background: color-mix(in srgb, var(--inverse), transparent 10%);
                    color: var(--color);
                }
            }
            
            .liability-warning {
                display: flex;
                flex-direction: row;
                gap: 1em;
                margin: 1em 0;
                
                .symbol {
                    font-family: "Iosevka Expanded", system-ui;
                    font-size: 2em;
                    width: min-content;
                    user-select: none;
                }
                
                .text {
                    margin: 0;
                }
            }
        </style>
    {/snippet}
    
    {@render liability(lessLegalese)}
    
    <button onclick={() => (lessLegalese = !lessLegalese)}>Read this section in {lessLegalese ? 'uppercase' : 'lowercase'}</button>
    
    <h3 id="severability">Severability</h3>
    
    <p>
        If a court finds one or more of these clauses unenforceable, the rest of these terms remain in effect.
    </p>

    <h3 id="contact">Contact</h3>

    <p>You can contact us at <a href={template.contactUri}>{template.contactName}</a></p>

    <h2 id="privacy-policy">Privacy policy</h2>

    <p>This section details how we process your data and how to object to the processing of your data.</p>

    <h3 id="data-collected">What information do we collect and why?</h3>

    <p>We collect the following information:</p>

    <ol>
        {#each template.collectedInformation as data (data.data)}
            <li>
                {data.data}
                <span class="faint">This is collected {data.why}.</span>
            </li>
        {/each}
    </ol>

    {#if template.genai}
        <h3 id="genai">Generative AI</h3>

        <p>
            Your data may be processed with Generative AI. If you object to this, do not use the service. Your content {template.genaiTraining
                ? 'is'
                : 'is not'} used to train Generative AI models.
        </p>

        <p>Generative AI is used to:</p>

        <ol>
            {#each template.genaiUses as use (use)}
                <li>{use}</li>
            {/each}
        </ol>
    {/if}

    <h3 id="dpa">Who processes my data?</h3>

    <p>Your data is shared with the following subprocessors solely for the purpose of providing the service to you:</p>

    <ol>
        {#each template.subprocessors as subprocessor (subprocessor.who)}
            <li><a href={subprocessor.dpa}>{subprocessor.who}</a></li>
        {/each}
    </ol>

    <h3 id="data-storage">How is my data stored?</h3>

    <p>Your data is {template.dataStorage}.</p>

    <p>Your data is stored for the following retention period: {template.dataRetention}</p>

    <h3 id="data-deletion">How do I delete my data?</h3>

    <p>You can request that your data is deleted.</p>

    {#if template.dataDeletion}
        <p>You can do so here: <a href={template.dataDeletion.method}>{template.dataDeletion.uri}</a></p>
    {:else}
        <p>Contact us using: <a href={template.contactUri}>{template.contactName}</a></p>
    {/if}
    
    <p>We must delete your data within a calendar month.</p>

    <h3 id="data-rights">What are my rights as a data subject?</h3>

    <p>Under the Data Protection Act 2018, you have the following rights:</p>

    <table>
        <thead>
            <tr>
                <th scope="col">Term</th>
                <th scope="col">Value</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th scope="row">The right to be informed</th>
                <td>
                    We must tell you what personal data we collect, why we collect it, for how long, and if we share
                    your personal data with third parties.
                </td>
            </tr>
            <tr>
                <th scope="row">The right to access</th>
                <td> You have the right to know what information we hold about you. </td>
            </tr>
            <tr>
                <th scope="row">The right to rectification</th>
                <td> We must update our records of you if you tell us that they are wrong. </td>
            </tr>
            <tr>
                <th scope="row">The right to erasure</th>
                <td> We must delete or anonymise your personal data that we hold about you. </td>
            </tr>
            <tr>
                <th scope="row">The right to restrict processing</th>
                <td> You have the right to ask us to limit the ways in which we process your personal data. </td>
            </tr>
            <tr>
                <th scope="row">The right to data portability</th>
                <td> You have the right to obtain and reuse your personal data across different services. </td>
            </tr>
            <tr>
                <th scope="row">The right to object</th>
                <td>
                    You may object to our processing of your personal data that is collected for legitimate interests.
                </td>
            </tr>
        </tbody>
    </table>

    <p>To use your rights, please use the contact method at the top of this page.</p>

    <p>
        This is not legal advice. Learn more on <a href="https://ico.org.uk/for-the-public/">ico.org.uk</a>
    </p>

    <h3 id="data-contact">Who do I contact regarding my personal data?</h3>

    <p>You can contact us at <a href={template.contactUri}>{template.contactName}</a></p>
</main>

<style>
    .faint {
        opacity: 0.6;
    }
</style>
