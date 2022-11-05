<script>
    export let isOpen = false;
</script>

{#if isOpen}
    <div class="backdrop" on:click|self>
        <div class="modal">
            <slot />
        </div>
    </div>
{/if}

<style>
    .backdrop {
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        position: fixed;
    }
    .modal {
        background-color: white;
        margin: 10% auto;
        max-width: 400px;
        padding: 10px;
        border-radius: 6px;
        text-align: center;
    }
</style>
