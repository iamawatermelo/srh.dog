<script lang="ts">
    import type { SVGAttributes } from 'svelte/elements';

    const attributes: SVGAttributes<SVGElement> = $props();
</script>

<svg
    class="flex-none"
    width="50"
    height="24"
    viewBox="0 0 50 24"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    {...attributes}
>
    <circle
        cx="8"
        cy="16"
        r="6"
        stroke="currentColor"
        stroke-width="4"
    />
    <path d="M24 0L16 24H21L29 0H24Z" fill="currentColor" />
    <path d="M29 0L37 24H32L24 0H29Z" fill="currentColor" />
    <path d="M36 12L32 24H37L41 12H36Z" style="fill: var(--accent)" />
    <path d="M44 12L40 24H45L49 12H44Z" style="fill: var(--accent)" />
</svg>