<script>
    import Logo from '$lib/Logo.svelte';
</script>

<svelte:head>
    <title>Sarah Pawton</title>
    <meta name="description" content="USER REPORT: 390119 SARAH PAWTON at 13:26 05/07/2025" />
</svelte:head>

<main>
    <div class="prelude">
        <Logo class="logo" aria-hidden="true" />

        <div class="term">
            <div style="grid-area: 1 / 1 / 2 / 2">#AWTDASP</div>
            <div style="grid-area: 1 / 2 / 2 / 3; text-align: center;" class="mob-right">Detailed User Display</div>
            <div style="grid-area: 1 / 3 / 2 / 4; text-align: right;" class="mob-hide">05/07/2025&nbsp;13:26</div>
            <div style="grid-area: 2 / 1 / 3 / 2" class="mob-hide" aria-hidden="true">==></div>
            <div style="grid-area: 2 / 2 / 3 / 4; text-align: right;" class="mob-hide">
                All sectors; WTT times; Page&nbsp;1..&nbsp;of&nbsp;1
            </div>
            <div style="grid-area: 3 / 1 / 3 / 4" aria-hidden="true">&nbsp;</div>
            <div style="grid-area: 4 / 1 / 5 / 4">USER REPORT: 390119 SARAH PAWTON at 13:26 05/07/2025</div>
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
                <td>dog</td>
            </tr>
            <tr>
                <th scope="row">Subject ID</th>
                <td class="type">u64</td>
                <td>390119</td>
            </tr>
            <tr>
                <th scope="row">Occupation</th>
                <td class="type">string</td>
                <td>student</td>
            </tr>
            <tr>
                <th scope="row">Last seen</th>
                <td class="type">location</td>
                <td>SJ711547 <span class="aside faint">EPSG:27700</span></td>
            </tr>
            <tr>
                <th scope="row">Connections</th>
                <td class="type">array&lt;link&gt;</td>
                <td>
                    <ol>
                        <li>
                            <a href="https://www.linkedin.com/in/sarah-pawton/">Sarah Pawton on LinkedIn</a>
                        </li>
                        <li>
                            <a href="https://github.com/iamawatermelo">iamawatermelo on GitHub</a>
                        </li>
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">Featured works</th>
                <td class="type">array&lt;link&gt;</td>
                <td>
                    <ol>
                        <li>
                            <a href="https://github.com/iamawatermelo/wakapi-anyide">wakapi-anyide</a><br />
                            <div class="faint">Time tracking tools to help global teenagers step into programming</div>
                        </li>
                        <li>
                            <a href="https://github.com/iamawatermelo/maybe-material">Maybe Material</a><br />
                            <div class="faint">72 vibrant, harmonious themes for Zed, built with colour science</div>
                        </li>
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">Nature of business</th>
                <td class="type">enumeration</td>
                <td>
                    62012 <span class="aside faint">Business and domestic software development</span>
                </td>
            </tr>
            <tr>
                <th scope="row">Stack trace</th>
                <td class="type">string</td>
                <td>
                    Tainted:
                    <abbr title="theriantropy">&Theta;&Delta;</abbr>
                    <abbr title="agender">&#x26B2;</abbr>
                    <abbr title="plural">&amp;</abbr>
                    <abbr title="polyamorous">&pi;</abbr>
                    <br />RIP: dump_stack+0x19/0x1b
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
                <th scope="row">Formed of</th>
                <td class="type">array&lt;entity&gt;</td>
                <td>
                    <ol>
                        <li>350121 Natalie</li>
                        <li>067008 Valerie</li>
                        <li>390121 Willow</li>
                        <li>777053 Ashley</li>
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">Related entities</th>
                <td class="type">array&lt;link&gt;</td>
                <td>
                    <ol>
                        <li>
                            <a href="https://transcental.dev/">transcental.dev</a>
                        </li>
                    </ol>
                </td>
            </tr>
        </tbody>
    </table>

    <footer class="term">
        <div style="grid-area: 1 / 1 / 4 / 4" aria-hidden="true">&nbsp;<br /><br /><br /></div>
        <div style="grid-area: 4 / 1 / 5 / 2" aria-hidden="true">[RO] SCR1 WCAG&nbsp;2.0&nbsp;WAI&#8209;AA</div>
        <div style="grid-area: 4 / 2 / 5 / 4; text-align: right;">(c)&nbsp;Landtable Surveillance</div>
        <div style="grid-area: 5 / 1 / 6 / 4" aria-hidden="true">&nbsp;</div>
        <div style="grid-area: 6 / 2 / 7 / 3">
            <a href="/embedding.txt" class="noarrow"><img src="/button.gif" alt="srh.dog" class="x88x31" /></a>
        </div>
    </footer>
</main>

<style>
    main {
        margin: auto;
        padding: 1em;
        margin-top: 4em;
        max-width: 48em;

        @media (max-width: 32em) {
            margin-top: 2em;
        }
    }

    a,
    a:visited {
        color: var(--accent);
        text-decoration: dotted underline;

        &:not(.noarrow)::after {
            display: inline-block;
            text-decoration: none;
            transition: transform 100ms;
            padding-left: 1ch;
            content: '->' / '';
        }

        &:hover {
            text-decoration-style: solid;
        }

        &:hover::after {
            transform: translateX(1ex);
        }
    }

    abbr {
        /* deliberately inaccessible */
        text-decoration: none;
    }

    div {
        margin: 0;
    }

    h1 {
        font-family: 'Iosevka Expanded', system-ui;
        margin-top: 1em;
    }

    :global(.logo) {
        width: 4em;
        height: 4em;
        margin-bottom: 2em;

        @media (max-width: 24em) {
            width: 2em;
            height: 2em;
            margin-bottom: 1em;
        }
    }

    @media (min-width: 64em) {
        .prelude {
            position: relative;
        }

        :global(.logo) {
            position: absolute;
            left: -6em;
        }
    }

    .term {
        font-feature-settings: 'calt' off;
        column-gap: 1ch;
        opacity: 0.6;
        user-select: none;

        display: grid;
        grid-template-columns: repeat(3, 1fr);

        @media (max-width: 32em) {
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

    table {
        display: grid;
        grid-auto-flow: row;
        grid-template-columns: max-content max-content 1fr;
        column-gap: 2em;

        text-align: left;

        thead,
        tbody,
        tr {
            display: grid;
            grid-template-columns: subgrid;
            grid-column: 1 / 4;
        }

        thead {
            color: var(--accent);
            font-size: 0.8em;
            text-transform: uppercase;

            tr {
                padding: 0.5em;

                border-bottom: 1px dashed color-mix(in srgb, var(--accent), transparent 60%);
            }
        }

        tbody tr {
            padding: 0.5em;

            &:not(:last-child) {
                border-bottom: 1px dashed #ffffff55;
            }
        }

        th {
            font-weight: normal;
        }

        .faint {
            opacity: 0.6;
        }

        .aside {
            display: inline-block;
        }

        .type {
            color: var(--accent);
            opacity: 0.8;
        }
    }

    ol {
        display: grid;
        grid-template-columns: min-content 1fr;

        margin: 0;
        padding: 0;
        list-style-type: none;
        counter-reset: list -1;

        li {
            display: grid;
            grid-template-columns: subgrid;
            grid-column: 1 / 3;
            counter-increment: list 1;

            > * {
                grid-column: 2;
            }

            &::before {
                grid-column: 1;
                width: max-content;
                opacity: 0.6;
                content: '- ' counter(list) ':' / '';
                padding-left: 2ch;
                padding-right: 1ch;
            }
        }

        &::after {
            grid-area: 1 / 1 / 2 / 3;
            counter-increment: list 1;
            width: max-content;
            opacity: 0.6;
            content: '+ Array [' counter(list) ']' / '';
        }
    }

    .x88x31 {
        width: 88px;
        height: 31px;
        
        display: block;
        margin: auto;
        image-rendering: pixelated;
    }

    /* Small width devices: Move type underneath the term */

    @media (max-width: 48em) {
        table {
            grid-template-columns: 1fr min-content;
            grid-auto-flow: column;

            thead,
            tbody,
            tr {
                grid-column: 1 / 3;
            }

            thead tr,
            tbody tr {
                padding: 1em 0.5em;
            }

            tr {
                row-gap: 0.5em;

                > *:nth-child(1) {
                    grid-column: 1;
                    opacity: 0.6;
                }

                > *:nth-child(2) {
                    grid-column: 2;
                    text-align: right;
                }

                > *:nth-child(3) {
                    grid-column: 1 / 3;
                }
            }
        }
    }
</style>
