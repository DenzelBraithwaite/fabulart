<script>
    export let textColor = 'text-black';
    export let bgColor = 'bg-none';
    export let shape = 'square'
    export let url = '/'
    export let border = false;
    $: classes = `${textColor} ${bgColor} ${shape}`
</script>

<!-- TODO:
- Make button shape settable from outside✅
- Make text color settable from outside✅
- Make background color settable from outside✅
- Make border settable from outside
- Make border color settable from outside



-->
{#if border}
<a href="{url}" class="btn border {classes}"><slot>Try me</slot></a>
{:else}
<a href="{url}" class="btn no-border {classes}"><slot>Try me</slot></a>
{/if}

<style>
    .btn:link,
    .btn:visited {
        display: inline-block;
        text-decoration: none;
        color: #fff;
        text-align: center;
        padding: 0.5rem 1rem;
    }

    .btn:hover,
    .btn:active {
        cursor: pointer;
    }

    .border {
        border: 1px solid blue;
    }

    .no-border {
        border: none;
        background-color: transparent;
    }

    .round {
        border-radius: 100px;
    }

    .square {
        border-radius: 5px;
    }

    .text-white {
        color: #fff;
    }

    .text-black {
        color: #2b2b2b;
    }

    .bg-cyan {
        background-color: cyan;
    }

    .bg-none {
        background-color: none;
    }
</style>