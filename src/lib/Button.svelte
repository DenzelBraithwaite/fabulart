<script>
    export let textColor = 'text-black';
    export let bgColor = 'bg-none';
    export let shape = 'square'
    export let url = '/'
    export let border = false;
    export let borderColor = 'border-peach';
    $: classes = `${textColor} ${bgColor} ${shape}`
</script>

<!-- TODO:
- Make button shape settable from outside ✅
- Make text color settable from outside ✅
- Make background color settable from outside ✅
- Make border settable from outside ✅
- Make border color settable from outside ✅ -->

{#if border}
<a href="{url}" class="btn border {classes} {borderColor}"><slot>Try me</slot></a>
{:else}
<a href="{url}" class="btn no-border {classes}"><slot>Try me</slot></a>
{/if}

<style>
    .btn:link,
    .btn:visited {
        display: inline-block;
        text-decoration: none;
        text-align: center;
        padding: 0.5rem 1rem;
    }

    .btn:hover,
    .btn:active {
        cursor: pointer;
    }

    /* Border styles */
    .border {
        border: 2px solid transparent;
        font-weight: 700;
    }

    .no-border {
        border: none;
        background-color: transparent;
    }

    .border-peach {
        border-color: #D98684;
    }

    .border-yellow {
        border-color: #FAD9A1;
    }

    .border-blue {
        border-color: #339af0;
    }

    .border-red {
        border-color: #fa5252;
    }

    .border-green {
        border-color: #51cf66;
    }

    /* Button shape */
    .round {
        border-radius: 100px; 
    }

    .square {
        border-radius: 0.25rem; /* 4px */
    }

    /* Text colors */
    .text-white {
        color: #fff;
    }

    .text-black {
        color: #2b2b2b;
    }

    .text-peach {
        color: #D98684;
    }

    .text-yellow {
        color: #FAD9A1;
    }

    .text-blue {
        color: #339af0;
    }

    .text-red {
        color: #fa5252;
    }

    .text-green {
        color: #51cf66;
    }

    /* Background colors */
    .bg-none {
        background-color: transparent;
    }

    .bg-peach {
        background-color: #D98684;
    }

    .bg-yellow {
        background-color: #FAD9A1;
    }

    .bg-blue {
        background-color: #339af0;
    }

    .bg-red {
        background-color: #fa5252;
    }

    .bg-green {
        background-color: #51cf66;
    }
</style>