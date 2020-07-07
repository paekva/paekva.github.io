<script>
    export let title;
    export let items = [];
</script>

<div class="listWrapper">
    <div class="title">{title}</div>
    <div>
        {#if items.length > 0}
            {#each items as item}
                <div class="item">
                    <div class="header">
                        <div class="label">{item.label}</div>
                        {#if item.date !== undefined} <div class="date">{item.date}</div> {/if}
                    </div>

                    <div class="description">{item.description}</div>
                </div>
            {/each}
        {/if}
    </div>
</div>

<style>
    .listWrapper {
        margin-bottom: 10px;
    }

    .title {
        padding: 8px;
        background: #cccccc;

        font-weight: bold;
    }

    .item {
        padding: 8px;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .label {
        font-weight: bold;
    }

    .date {
        font-style: italic;
    }

    .header {
        display: flex;
        flex-direction: row;

        justify-content: space-between;
    }
</style>