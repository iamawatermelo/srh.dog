<script lang="ts">
    import ContractTemplate from '$lib/legal/ContractTemplate.svelte';
</script>

{#snippet tou()}
    <p>
        The agent is designed to generate &ldquo;edgy&rdquo; content. However, you may not, through instructing the
        agent or through implying it should do so:
    </p>

    <ol>
        <li>
            use the agent to generate outputs, including child sexual abuse material, that exploit or sexualise children
        </li>
        <li>
            use the agent to generate suicide or self-harm content, including eating disorders, or generate content to
            facilitate activities that may cause real-world harm, like instructions on how to purchase illegal drugs or
            guides for building weapons
        </li>
        <li>use the agent to depict excessive blood, gore or injuries, or gratuitous violence against animals</li>
        <li>use the agent to incite violence, make malicious attacks or bully or threaten individuals or groups</li>
        <li>
            use the agent to generate pornography, erotic content, depictions of rape, sexual assault or sexual abuse
        </li>
    </ol>

    <p>If you are found to be in violation of these rules your access to the service may be removed.</p>
{/snippet}

<ContractTemplate
    template={{
        what: 'the Valerie agent',
        id: 'valerie/torment-tos',
        providingEntity: 'Sarah Pawton',
        lastUpdated: new Date(2026, 1, 23),
        contactName: 'policy@srh.dog',
        contactUri: 'mailto:policy@srh.dog',
        changeNotifications: 'by Discord announcement',

        minimumAge: 16,
        extraSections: [
            {
                header: 'Please be nice',
                body: tou
            }
        ],

        collectedInformation: [
            {
                data: 'your complete Discord profile, including your username, current nickname, pronouns and about me',
                why: 'to be able to address and respond to you, and remember important facts about you'
            },
            {
                data: "any message content you send in Valerie's thread",
                why: 'to be able to respond to you'
            },
            {
                data: 'any content Valerie reads while she is active in a thread',
                why: 'to be able to respond to you'
            }
        ],
        subprocessors: [
            {
                who: 'Google Cloud',
                dpa: 'https://cloud.google.com/terms/data-processing-addendum'
            }
        ],
        dataRetention: 'at most 5 years from your last interaction, or one calendar month after you leave the server',
        dataStorage: 'encrypted at rest in Google Cloud',

        genai: true,
        genaiTraining: false,
        genaiUses: ['react and respond to you', 'remember information about you']
    }} />
