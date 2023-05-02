<script>
    import '@fortawesome/fontawesome-free/css/all.css';
    export let backgroundColor = '';
    export let logoCentered = false;
</script>

{#if logoCentered}
    <nav class="{backgroundColor}">
        <div class="wrapper">
            <i class="fa-solid fa-book-open"></i>
            <h1 class="nav-title">Fabulart</h1>
        </div>
        <div class="wrapper">
            <i class="fa-solid fa-share-nodes"></i>
            <i class="fa-solid fa-house"></i>
            <i class="fa-solid fa-user"></i>
        </div>
    </nav>
{:else}
    <nav class="{backgroundColor}">
        <div class="wrapper">
            <i class="fa-solid fa-book-open"></i>
        </div>
        <h1 class="nav-title">Fabulart</h1>
        <div class="wrapper">
            <i class="fa-solid fa-share-nodes"></i>
            <i class="fa-solid fa-house"></i>
            <i class="fa-solid fa-user"></i>
        </div>
    </nav>
{/if}

<style>
    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 1rem;
        margin-bottom: 3rem;
        width: 100%;
        transform: translate(-1rem); /* Only for utility kit page */
        margin-left: auto;
        margin-right: auto;
    }

    .nav-title {
        display: inline-block;
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