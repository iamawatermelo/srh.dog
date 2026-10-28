<script lang="ts">
    import Logo from '$lib/Logo.svelte';
    import { onMount } from 'svelte';

    let now = $state<Date | undefined>();

    const dateString = $derived(now ? now.toLocaleDateString(
        "en-GB",
        {
            year: "numeric",
            month: "2-digit",
            day: "2-digit",
            hour: "2-digit",
            minute: "2-digit",
            second: "2-digit"
        }
    ) : "");

    onMount(() => {
        now = new Date();
        let currentTimeout: number;

        currentTimeout = setTimeout(() => {
            now = new Date()
            currentTimeout = setInterval(() => {
                now = new Date()
            }, 1000)
        }, 1000 - now.getUTCMilliseconds());

        return () => {
            clearTimeout(currentTimeout);
        }
    })
</script>

<svelte:head>
    <title>Sarah Pawton</title>
    <meta name="description" content="Student interested in systems programming, app design, web accessibility, distributed systems and railway operations." />
</svelte:head>

<main>
    <div class="prelude">
        <Logo class="logo" aria-hidden="true" />

        <div class="term">
            <div style="grid-area: 1 / 1 / 2 / 2">#AWTDASP</div>
            <div style="grid-area: 1 / 2 / 2 / 3; text-align: center;" class="mob-right">Detailed User Display</div>
            <div style="grid-area: 1 / 3 / 2 / 4; text-align: right;" class="mob-hide">{dateString}</div>
            <div style="grid-area: 2 / 1 / 3 / 2" class="mob-hide" aria-hidden="true">==></div>
            <div style="grid-area: 2 / 2 / 3 / 4; text-align: right;" class="mob-hide">
                All sectors; WTT times; Page&nbsp;1..&nbsp;of&nbsp;1
            </div>
            <div style="grid-area: 3 / 1 / 3 / 4" aria-hidden="true">&nbsp;</div>
            <div style="grid-area: 4 / 1 / 5 / 4">USER REPORT: 390119 SARAH PAWTON at 18:05 27/10/2026</div>
        </div>
    </div>

    <h1>Sarah Pawton</h1>

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
                <th scope="row">Subject description</th>
                <td class="type">string</td>
                <td>
                    Student interested in systems programming, app design, web accessibility, distributed systems and
                    railway operations.
                </td>
            </tr>
            <tr>
                <th scope="row">Connections</th>
                <td class="type">array&lt;link&gt;</td>
                <td>
                    <ol>
                        <li>
                            <a href="https://www.linkedin.com/in/sarah-pawton/">Sarah Pawton on LinkedIn</a>
                        </li>
                        <!--
                        <li>
                            <a href="https://github.com/iamawatermelo">iamawatermelo on GitHub</a>
                        </li>
                        -->
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">Featured works</th>
                <td class="type">array&lt;link&gt;</td>
                <td>
                    <ol>
                        <li>
                            <a href="https://github.com/iamawatermelo/maybe-material">Maybe Material</a>
                            <div>
                                2026 <span class="faint"
                                    >72 vibrant, harmonious themes for Zed, built with colour science</span>
                            </div>
                        </li>
                        <li>
                            <a href="https://github.com/iamawatermelo/wakapi-anyide">wakapi-anyide</a>
                            <div>
                                2024 <span class="faint"
                                    >Time tracking tools to help teenagers step into programming</span>
                            </div>
                        </li>
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">Pronouns</th>
                <td class="type">array&lt;string&gt;</td>
                <td>
                    <ol>
                        <li>it/its</li>
                        <li>she/her</li>
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">Subject type</th>
                <td class="type">string</td>
                <td>dog</td>
            </tr>
            <tr>
                <th scope="row">Subject ID</th>
                <td class="type">u64</td>
                <td>390119</td>
            </tr>
            <tr>
                <th scope="row">Nature of business</th>
                <td class="type">enumeration</td>
                <td>
                    62012 <span class="aside faint">Business and domestic software development</span>
                </td>
            </tr>
            <tr>
                <th scope="row">Last seen</th>
                <td class="type">location</td>
                <td>SJ711547 <span class="aside faint">EPSG:27700</span></td>
            </tr>
            <tr>
                <th scope="row">Stack trace</th>
                <td class="type">string</td>
                <td>
                    Tainted:
                    <abbr title="theriantropy symbol">&Theta;&Delta;</abbr>
                    <abbr title="agender symbol">&#x26B2;</abbr>
                    <abbr title="plurality symbol">&amp;</abbr>
                    <abbr title="polyamory symbol">&pi;</abbr>
                    <br />RIP: dump_stack+0x19/0x1b
                </td>
            </tr>
            <tr>
                <th scope="row">Formed of</th>
                <td class="type">array&lt;entity&gt;</td>
                <td>
                    <ol>
                        <li><span>350121 Natalie <span class="faint">(+13 names)</span></span><span class="aside faint">it/its</span></li>
                        <li>390121 Willow <span class="aside faint">she/they</span></li>
                        <li>777053 Ashley <span class="aside faint">it/its</span></li>
                    </ol>
                </td>
            </tr>
        </tbody>
    </table>

    <footer class="term">
        <div style="grid-area: 1 / 1 / 4 / 4" aria-hidden="true">&nbsp;<br /><br /><br /></div>
        <div style="grid-area: 4 / 1 / 5 / 2" aria-hidden="true">[RO] SCR1</div>
        <div style="grid-area: 4 / 2 / 5 / 4; text-align: right;">(c)&nbsp;Landtable Surveillance</div>
        <div style="grid-area: 5 / 1 / 6 / 4" aria-hidden="true">&nbsp;</div>
        <div style="grid-area: 6 / 1 / 7 / 4; text-align: center;">
            <a href="/embedding.txt" class="noarrow">
                <img src="/button-dark.gif" alt="srh.dog" loading="lazy" class="x88x31 dark" />
                <img src="/button-light.gif" alt="srh.dog" loading="lazy" class="x88x31 light" />
            </a>
            <!--
            <div class="buttons">
                <a href="https://prpl.wtf/" class="noarrow">
                    <img src={Prpl} alt="prpl.wtf" loading="lazy" class="x88x31" />
                </a>
                <a href="https://auri.lol/" class="noarrow">
                    <img src={Auri} alt="auri.lol" loading="lazy" class="x88x31" />
                </a>
            </div>
            -->
        </div>
    </footer>
</main>

<style>
    abbr {
        /* deliberately inaccessible */
        text-decoration: none;
    }

    .term {
        font-feature-settings:
            'ss20',
            'calt' off;
        column-gap: 1ch;
        opacity: 0.6;

        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));

        @media (max-width: 38em) {
            .mob-hide {
                display: none;
            }

            /* i'm as upset as you are that i'm using !important */

            .mob-right {
                grid-column: 2 / 4 !important;
                text-align: right !important;
            }
        }
    }

    /*
    .buttons {
        padding-top: 2em;
        display: flex;
        justify-content: center;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 1em;
    }
    */

    :global(.logo) {
        margin-bottom: 2em;
    }

    @media (min-width: 64em) {
        .prelude {
            position: relative;
        }

        :global(.logo) {
            position: absolute;
            left: -6em;
            transform: scale(1.5)
        }
    }
</style>
