<script lang="ts">
    import ContractTemplate from '$lib/legal/ContractTemplate.svelte';
</script>

<ContractTemplate
    template={{
        what: 'the Valerie file sharing service',
        id: 'valerie/files-tos',
        providingEntity: 'Sarah Pawton',
        lastUpdated: new Date(2026, 9, 28),
        contactName: 'policy@srh.dog',
        contactUri: 'mailto:policy@srh.dog',
        changeNotifications: 'by Discord announcement',

        minimumAge: 16,
        extraSections: [],

        collectedInformation: [
            {
                data: 'the files you upload',
                why: 'to be able to provide the file sharing service'
            },
            {
                data: "your Discord User ID, the Channel ID and Interaction ID",
                why: 'to be able to respond to you'
            },
        ],
        subprocessors: [],
        dataRetention: 'until you delete the file',
        dataStorage: 'stored on-premises and not encrypted',

        genai: false,
        genaiTraining: false,
        genaiUses: []
    }} />
