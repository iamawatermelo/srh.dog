<script lang="ts">
    import ContractTemplate from '$lib/legal/ContractTemplate.svelte';
</script>

<ContractTemplate
    template={{
        what: 'Wordle Bot',
        id: 'valerie/wordle-bot-tos',
        providingEntity: 'Sarah Pawton',
        lastUpdated: new Date(2026, 1, 23),
        contactName: 'policy@srh.dog',
        contactUri: 'mailto:policy@srh.dog',
        changeNotifications: 'by Discord announcement',

        minimumAge: 16,
        extraSections: [],

        collectedInformation: [
            {
                data: 'your uploaded Wordle screenshot',
                why: 'to provide the service'
            }
        ],
        subprocessors: [
            {
                who: 'Google Cloud',
                dpa: 'https://cloud.google.com/terms/data-processing-addendum'
            }
        ],
        dataRetention: 'not retained',
        dataStorage: 'not stored',

        genai: true,
        genaiTraining: false,
        genaiUses: ['process your screenshot']
    }} />
