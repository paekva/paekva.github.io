<script>
    export let name;
    export let picUrl;
    export let description;
</script>

<div class="profileWrapper">
    <div class="picture">
        <img src={picUrl} />
    </div>
    <div class="name">{name}</div>
    <div class="description">{description}</div>
</div>

<style>
    .profileWrapper{
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .picture {
        border: 1px solid #666666;
        height: 192px;
        border-radius: 50%;
    }

    .name, .description {
        text-align: center;
    }
</style>