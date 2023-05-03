<script>
    import Button from '$lib/Button.svelte';

    export let btnColor = 'bg-red';
    export let type;
</script>

<!-- Onboarding / Greeting Modal -->
{#if type === 'onboarding'}
    <div class="backdrop">
        <div class="modal">
            <i class="fa-solid fa-x btn-close"></i>
            <div class="text-wrapper">
                <h2 class="title"><slot name="title"/></h2>
                <p class="message"><slot name="message"/></p>
            </div>
            <Button bgColor="{btnColor}" textColor="text-white"><slot name="button"/></Button>
        </div>
    </div>
    {:else if type === 'warning'}
    <div class="backdrop">
        <div class="modal">
            <i class="fa-solid fa-x btn-close"></i>
            <div class="text-wrapper">
                <h2 class="warning-title"><slot name="title"/></h2>
                <p class="message"><slot name="message"/></p>
            </div>
            <div class="btn-wrapper">
                <Button bgColor="bg-red" textColor="text-white"><slot name="btn-accept"/></Button>
                <Button border={true} borderColor="border-grey" textColor='text-grey'><slot name="btn-refuse"/></Button>
            </div>
        </div>
    </div>
{:else if type === 'new-feature'}
    <div class="backdrop">
        <div class="feature-modal">
            <div class="title-section">
                <i class="fa-solid fa-x btn-close"></i>
                <h2 class="feature-title"><slot name="title"/></h2>
            </div>
            <p class="feature-message"><slot name="message"/></p>
            <div class="feature-btn-wrapper">
                <Button bgColor="{btnColor}" textColor="text-white"><slot name="button"/></Button>
            </div>
        </div>
    </div>
{/if}

<style>
    .backdrop {
        position: relative;
        background-color: #000000ce;
        height: 500px;
    }

    .modal {
        width: 50%;
        margin: 0 auto;
        background-color: #fff;
        padding: 3rem 3rem 2rem;
        text-align: center;

        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        border-radius: 0.25rem;
    }

    .text-wrapper {
        width: 100%;
        margin: 0 auto;
        margin-bottom: 2rem;
    }

    .btn-wrapper {
        display: flex;
        justify-content: center;
        gap: 2rem;
    }

    .title {
        font-size: 1.5rem;
        margin-bottom: 2rem;
    }

    .message {
        font-size: 1rem;
        line-height: 1.3;
    }

    .btn-close {
        position: absolute;
        top: 1rem;
        right: 1rem;
    }

    /* Modal type: Warning */ 
    .warning-title {
        color: #fa5252;
        font-size: 1.5rem;
        margin-bottom: 2rem;
    }

    /* Modal type: New-feature */
    .feature-modal {
        width: 50%;
        margin: 0 auto;
        background-color: #fff;
        /* padding: 1rem; */
        border-radius: 0.25rem;

        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .title-section {
        text-align: start;
        padding: 1rem 0;
        background-color: #8284d8;
        margin-bottom: 1.5rem;
        border-radius: 0.25rem 0.25rem 0 0;
    }

    .feature-title {
        color: #fff;
        padding-left: 1.5rem;
    }

    .feature-message {
        line-height: 1.3;
        padding-left: 1.5rem;
        font-size: 1rem;
        margin-bottom: 2rem;
    }

    .feature-btn-wrapper {
        margin-left: 1.5rem;
        margin-bottom: 1.5rem;
    }
</style>