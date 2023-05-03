<script>
    import Button from '$lib/Button.svelte';
</script>

<div class="backdrop">
    <div class="modal">
        <i class="fa-solid fa-x btn-close"></i>
        <div class="text-wrapper">
            <h2 class="title">Modal title here?</h2>
            <p class="message">Labore ad adipisci accusamus atque odit illo temporibus minima! Aspernatur consequatur qui cumque, atque, dolore quod aliquam voluptas repellendus, magnam magni eos.</p>
        </div>
        <Button bgColor="bg-pink" textColor="text-white">Close</Button>
    </div>
</div>

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
        padding: 3rem;
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
        margin-bottom: 3rem;
    }

    .title {
        font-size: 1.5rem;
        margin-bottom: 2rem;
    }

    .message {
    }

    .btn-close {
        position: absolute;
        top: 1rem;
        right: 1rem;
    }
</style>