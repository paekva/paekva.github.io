<script>
    import SideMenuItem from "./SideMenuItem.svelte";
    import * as constant from '../constants';

    export let selectedItem;
    export let itemClickHandler;
</script>

{#if constant.menuItems.length > 0}
    {#each constant.menuItems as item}
        <SideMenuItem
                itemLabel={item.label}
                selected={item.id === selectedItem}
                onItemClick={() => itemClickHandler(item.id)}
        />
    {/each}
{/if}