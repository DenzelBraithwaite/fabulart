<script>
    import Layout from '../routes/layout.svelte';
    export let action = '/';
    export let newStory = true;
    export let bgColor = 'bg-pink';

    function submitHandler() {
        // Do something when the form gets submitted
        console.log('form submitted');
    }
</script>
<!-- TODO: make all id's unique, even if they're conditionally rendered, example: id=img-description-->

<!-- The svelte:component is to apply global css from the src/routes/__layout.svelte file -->
<svelte:component this={Layout}>
{#if newStory}
    <form on:submit|preventDefault={submitHandler} action="{action}" class="{bgColor}">
        <h2 class="form-title-pink">Create your story!</h2>
        <div class="form-control">
            <input type="text" id="title" name="title" placeholder="Enter your story title here">
        </div>
        <div class="form-control">
            <textarea name="img-description" id="img-description" placeholder="Describe the image you would like to see! Example, friends playing soccer outiside on a sunny day!"></textarea>
        </div>
        <button type="submit">Create</button>
    </form>
{:else}
    <form on:submit|preventDefault={submitHandler} action="{action}" class="{bgColor}">
        <h2 class="form-title-pink">Create another page!</h2>
        <div class="form-control">
            <textarea name="img-description" id="img-description" placeholder="Describe the image you would like to see! Example, friends playing soccer outiside on a sunny day!"></textarea>
        </div>
        <div class="form-control">
            <textarea name="page-description" id="page-description" placeholder="Write the text that goes with the image here!"></textarea>
        </div>
        <button type="submit">Add</button>
    </form>
{/if}
</svelte:component>

<style>
    form {
        position: relative;
        box-shadow: 0 4px 8px #0000002c;
        width: 50%;
        max-width: 500px;
        margin: 0 auto 2rem;
        text-align: center;
        padding: 2rem 1rem;
        border-radius: 0.5rem;
    }

    .form-control {
        position: relative;
        width: 100%;
        margin: 2rem 0;
    }

    input {
        outline: none;
        border: none;
        padding: 0.25rem;
        width: 90%;
        border: 2px solid #b7b7b7;
        border-radius: 0.25rem;
    }

    textarea {
        padding: 0.25rem;
        min-width: 90%;
        max-width: 90%;
        min-height: 100px;
        border: 2px solid #b7b7b7;
        border-radius: 0.25rem;
        max-height: 300px;
    }

    .bg-pink textarea,
    .bg-pink input {
        background-color: #fff2f1;
    }

    .bg-yellow textarea,
    .bg-yellow input {
        background-color: #fff9ef;
    }

    textarea::placeholder {
        /* If you want to style the placeholder text (ex: color) */
    }

    textarea:focus,
    input:focus {
        /* outline: 2px solid #D98684; */
        outline: none;
        border: 2px solid #D98684;
    }

    button {
        border: none;
        display: inline-block;
        text-decoration: none;
        text-align: center;
        padding: 0.75rem 1.5rem;
        border-radius: 0.25rem;
        box-shadow: 0 4px 8px #00000018;
        color: #fff;
        background-color: #D98684;
    }

    button:hover,
    button:active {
        cursor: pointer;
    }

    /* Background Colors */
    .bg-none {
        background-color: transparent;
    }

    .bg-grey {
        background-color: #e9e9e9;
    }

    .bg-pink {
        background-color: #ffdfde;
    }

    .bg-yellow {
        background-color: #ffedcf;
    }

    /* Accent colors (title, input outline, button bg) */
    .form-title-pink {
        color: #D98684;
    }

    .form-outline-pink {
        outline: #D98684;
    }

    .btn-pink {
        background-color: #D98684;
    }

    .form-title-yellow {
        color: #FAD491;
    }

    .form-outline-yellow {
        outline: #FAD491;
    }

    .btn-yellow {
        background-color: #FAD491;
    }
</style>