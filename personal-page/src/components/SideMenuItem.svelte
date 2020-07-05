<script>
    export let itemLabel;
    export let selected;
    export let onItemClick;
</script>

<div class={selected ? "selectedItem" : "item"} on:click={onItemClick}>
    {itemLabel}
</div>

<style>
    .item, .selectedItem {
        flex: 1;
        width: inherit;
        color: crimson;

        text-align: center;
        padding: 8px;

        cursor: pointer;
    }

    .selectedItem {
        font-weight: bold;
        background: #ccccff;
    }

    .item:hover, .selectedItem:hover {
        background: #cccccc;
        font-weight: bold;
    }
</style>