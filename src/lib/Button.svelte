<script>
    export let textColor = 'text-black';
    export let bgColor = 'bg-none';
    export let shape = 'square'
    export let url = '/'
    export let border = false;
    export let borderColor = 'border-pink';
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
        padding: 0.75rem 1.125rem;
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
    
    .border-grey {
        border-color: #a5a5a5;
    }

    .border-pink {
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

    .border-purple {
        border-color: #8284d8;
    }

    /* Button shape */
    .round {
        border-radius: 100px; 
    }

    .square {
        border-radius: 0.25rem; /* 4px */
    }

    /* Text colors */
    .text-grey {
        color: #a5a5a5;
    }

    .text-white {
        color: #fff;
    }

    .text-black {
        color: #a5a5a5;
    }

    .text-pink {
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

    .text-purple {
        color: #8284d8;
    }

    /* Background colors */
    .bg-none {
        background-color: transparent;
    }

    .bg-grey {
        background-color: #a5a5a5;
    }

    .bg-danger {
        background-color: red;
    }

    .bg-pink {
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

    .bg-purple {
        background-color: #8284d8;
    }
</style>