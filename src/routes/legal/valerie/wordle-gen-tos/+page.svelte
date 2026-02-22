<script lang="ts">
    let accessible = $state(false);
</script>

<main class:accessible>
    <h1>Terms of use and privacy policy for Wordle Bot</h1>

    <button onclick={() => (accessible = !accessible)}>Use system font</button>

    <p>
        By using the corresponding functionality in the bot (referred to as the "service") you agree to the following
        terms and privacy notice.
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
                <td>valerie/wordle-gen-tos</td>
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
                        <li>the image you provide to Valerie.</li>
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
                <td>No data is stored by Sarah or any subprocessors</td>
            </tr>
            <tr>
                <th scope="row">Data retention</th>
                <td class="type">enumeration</td>
                <td>No data is stored by Sarah or any subprocessors</td>
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
        <li>the image you provide to Valerie.</li>
    </ol>

    <p>This information is collected to provide the service.</p>

    <h3>Generative AI</h3>

    <p>This service uses Generative AI. If you object to this, do not use the service.</p>

    <p>Your data may be processed with Generative AI. Your content is not used to train Generative AI models.</p>

    <h3>Who processes my data?</h3>

    <p>A list of data subprocessors are at the top of this page.</p>

    <h3>How do you store my data?</h3>

    <p>Your data is not stored.</p>

    <h3>When will you delete my information?</h3>

    <p>Your data is not stored.</p>

    <h3>What are my rights as a data subject?</h3>

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

    <h3>Who do I contact regarding my personal data?</h3>

    <p>Please use the contact method at the top of this page.</p>
</main>
