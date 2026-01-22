<script>
	import Logo from '$lib/Logo.svelte';
</script>

<main>
    <Logo class="logo"/>
    
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
                <th scope="row">Nature of business</th>
                <td class="type">enumeration</td>
                <td>62012<br /><span class="faint">Business and domestic software development</span></td>
            </tr>
            <tr>
                <th scope="row">Connections</th>
                <td class="type">array&lt;link&gt;</td>
                <td>
                    <span class="faint pre">+ Array [2]</span>
                    <div class="array-item"><span class="faint pre">&nbsp;&nbsp;0:&nbsp;</span><a href="https://www.linkedin.com/in/sarah-pawton/">Sarah Pawton on LinkedIn</a></div>
                    <div class="array-item"><span class="faint pre">&nbsp;&nbsp;1:&nbsp;</span><a href="https://github.com/iamawatermelo">iamawatermelo on GitHub</a></div>
                </td>
            </tr>
            <tr>
                <th scope="row">Members</th>
                <td class="type">array&lt;object&gt;</td>
                <td>
                    <span class="faint pre">+ Array [4]</span>
                    <div class="array-item"><span class="faint pre">&nbsp;&nbsp;0:&nbsp;</span><span>Natalie</span></div>
                    <div class="array-item"><span class="faint pre">&nbsp;&nbsp;1:&nbsp;</span><span>Valerie</span></div>
                    <div class="array-item"><span class="faint pre">&nbsp;&nbsp;2:&nbsp;</span><span>Willow</span></div>
                    <div class="array-item"><span class="faint pre">&nbsp;&nbsp;3:&nbsp;</span><span>Ashley</span></div>
                </td>
            </tr>
            <tr>
                <th scope="row">Featured works</th>
                <td class="type">array&lt;link&gt;</td>
                <td>
                    <span class="faint pre">+ Array [2]</span>
                    <div class="array-item">
                        <span class="faint pre">&nbsp;&nbsp;0:&nbsp;</span>
                        <span>
                            <a href="https://github.com/iamawatermelo/wakapi-anyide">wakapi-anyide</a><br />
                            <span class="faint">Time tracking tools to help global teenagers step into programming</span>
                        </span>
                    </div>
                    <div class="array-item">
                        <span class="faint pre">&nbsp;&nbsp;1:&nbsp;</span>
                        <span>
                            <a href="https://github.com/iamawatermelo/maybe-material">Maybe Material</a><br />
                            <span class="faint">72 vibrant, harmonious themes for Zed, built with colour science</span>
                        </span>
                    </div>
                </td>
            </tr>
        </tbody>
    </table>
</main>

<style>
    :global(.logo) {
        width: 4em;
        height: 4em;
    }
    
    main {
        margin: auto;
        padding: 1em;
        margin-top: 4em;
        max-width: 48em;
    }
    
    a, a:visited {
        color: #66158A;
        text-decoration: dotted underline;
        
        &::after {
            display: inline-block;
            text-decoration: none;
            transition: transform 100ms;
            padding-left: 1ex;
            content: "->"
        }
        
        &:hover {
            text-decoration-style: solid;
        }
        
        &:hover::after {
            transform: translateX(1ex);
        }
    }
    
    table {
        display: grid;
        grid-auto-flow: row;
        grid-template-columns: max-content max-content 1fr;
        gap: 0.5em;
        
        font-family: 'Adwaita Mono', monospace;
        text-align: left;
        
        thead, tbody, tr {
            display: grid;
            grid-template-columns: subgrid;
            grid-column: 1 / 4;
        }
        
        thead {
            color: #66158A;
            font-size: 0.8em;
            text-transform: uppercase;
        }
        
        tbody {
            gap: 0.25em;
        }
        
        tr {
            gap: 2rem;
        }
        
        th {
            font-weight: normal;
        }
        
        .faint {
            opacity: 0.6;
        }
        
        .pre {
            white-space: pre;
        }
        
        .type {
            color: #66158A;
        }
        
        .array-item {
            display: flex;
            flex-direction: row;
        }
    }
    
    /* Small width devices: Move type underneath the term */
    
    @media (max-width: 48em) {
        table {
            grid-template-columns: 1fr min-content;
            grid-auto-flow: column;
            gap: 1em;
            
            thead, tbody, tr {
                grid-column: 1 / 3;
            }
            
            tbody {
                gap: 2em;
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
