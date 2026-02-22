<script lang="ts">
    let accessible = $state(false);
</script>

<main class:accessible>
    <h1>Terms of use and privacy policy for the Valerie agent</h1>

    <button onclick={() => (accessible = !accessible)}>Use {accessible ? 'website font' : 'system font'}</button>

    <p>
        By interacting with the Valerie agent (referred to as the "service") you agree to the following terms and
        privacy notice.
    </p>

    <h2>Notice summary</h2>

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
                <td>valerie/torment-tos</td>
            </tr>
            <tr>
                <th scope="row">Last updated</th>
                <td class="type">date</td>
                <td>22 February 2026</td>
            </tr>
            <tr>
                <th scope="row">Minimum age to use service</th>
                <td class="type">integer</td>
                <td>16</td>
            </tr>
            <tr>
                <th scope="row">Collected information</th>
                <td class="type">array&lt;string&gt;</td>
                <td>
                    <ol>
                        <li>
                            your complete Discord profile, including your username, current nickname, pronouns and about
                            me
                        </li>
                        <li>any message content you send in Valerie's thread</li>
                        <li>any content Valerie reads while she is active in a thread</li>
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">Data subprocessors</th>
                <td class="type">array&lt;link&gt;</td>
                <td>
                    <ol>
                        <li><a href="https://cloud.google.com/terms/data-processing-addendum">Google Cloud</a></li>
                    </ol>
                </td>
            </tr>
            <tr>
                <th scope="row">AI processing</th>
                <td class="type">enumeration</td>
                <td>This service processes your data with Generative AI</td>
            </tr>
            <tr>
                <th scope="row">AI training</th>
                <td class="type">enumeration</td>
                <td>Your content is not used to train Generative AI models</td>
            </tr>
            <tr>
                <th scope="row">Data storage</th>
                <td class="type">enumeration</td>
                <td>Your data is stored securely in Google Cloud</td>
            </tr>
            <tr>
                <th scope="row">Data retention</th>
                <td class="type">enumeration</td>
                <td>Indefinitely</td>
            </tr>
            <tr>
                <th scope="row">Data deletion</th>
                <td class="type">enumeration</td>
                <td>Manual, by contact</td>
            </tr>
            <tr>
                <th scope="row">Point of contact</th>
                <td class="type">email</td>
                <td>policy (at) srh.dog</td>
            </tr>
        </tbody>
    </table>

    <h2>Age restrictions</h2>

    <p>
        The minimum age to use this service is 16 years old. Users agree that they are over 16 years old or are known to
        be over 16 years old when they enter Valerie's server. Access will be restricted to users under 16.
    </p>

    <h2>Please be nice</h2>

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

    <h2>Limitation of liability</h2>

    <p>
        THE SERVICE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO
        THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL SARAH
        PAWTON OR ANY AFFILIATES BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
        TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SERVICE OR THE USE OR OTHER DEALINGS IN THE
        SERVICE.
    </p>

    <a href="https://opensource.org/license/mit">Adapted from the MIT License</a>

    <h2>Contact</h2>

    <p>Please use the contact method at the top of this page.</p>

    <h2>Privacy</h2>

    <h3>What information do we collect and why?</h3>

    <p>We collect the following information:</p>

    <ol>
        <li>your complete Discord profile, including your username, current nickname, pronouns and about me</li>
        <li>any message content you send in Valerie's thread</li>
        <li>any content Valerie reads while she is active in a thread</li>
    </ol>

    <p>This information is collected to provide the service.</p>

    <h3>Generative AI</h3>

    <p>This service uses Generative AI. If you object to this, do not use the service.</p>

    <p>Your data may be processed with Generative AI. Your content is not used to train Generative AI models.</p>

    <h3>Who processes my data?</h3>

    <p>A list of data subprocessors are at the top of this page.</p>

    <h3>How do you store my data?</h3>

    <p>Your data is stored in Google Cloud and is encrypted at rest.</p>

    <h3>When will you delete my information?</h3>

    <p>Your data is held until the agent's memories are destroyed.</p>

    <p>
        You may request that your data is deleted. To learn more about data deletion, please use the contact method at
        the top of this page.
    </p>

    <h3>What are my rights as a data subject?</h3>

    <p>Under the Data Protection Act 2018, you have the following rights:</p>

    <table>
        <thead>
            <tr>
                <th scope="col">Right</th>
                <th scope="col">Description</th>
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

    <h3>Who do I contact regarding my personal data?</h3>

    <p>Please use the contact method at the top of this page.</p>
</main>
