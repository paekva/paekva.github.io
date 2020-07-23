<script>
    export let clicked;
</script>

<div class="container">
    <div class={clicked ? "left exp" : "left"} on:click>

    </div>
    <div class="right">

    </div>
</div>

<style>
    .container {
        height: 100%;
        display: flex;
        flex-direction: column;
        background: yellow;
        position: relative;
        overflow: hidden;
    }


    @keyframes borders {
        0% {
            border: 14rem solid transparent;
            border-top: 14rem solid crimson;
            border-right: 14rem solid crimson;
        }
        40% {
            border-top: 17rem solid crimson;
            border-right: 28rem solid crimson;
            border-bottom: 16rem solid transparent;
            border-left: 28rem solid transparent;
        }
        75% {
            border-top: 21rem solid crimson;
            border-right: 43rem solid crimson;
            border-bottom: 17rem solid transparent;
            border-left: 34rem solid transparent;
        }
        80% {
            border-top: 30rem solid crimson;
            border-right: 47rem solid crimson;
            border-bottom: 17rem solid transparent;
            border-left: 34rem solid transparent;
        }
        85% {
            border-top: 37rem solid crimson;
            border-right: 67rem solid crimson;
            border-bottom: 17rem solid transparent;
            border-left: 34rem solid transparent;
        }
        90% {
            border-top: 53rem solid crimson;
            border-right: 85rem solid crimson;
            border-bottom: 17rem solid transparent;
            border-left: 34rem solid transparent;
        }
        95% {
            border-top: 60rem solid crimson;
            border-right: 100rem solid crimson;
            border-bottom: 17rem solid transparent;
            border-left: 34rem solid transparent;
        }
        100% {
            border-top: 19rem solid crimson;
            border-right: 40rem solid crimson;
            border-bottom: 18rem solid crimson;
            border-left: 40rem solid crimson;
        }
    }

    .left {
        top: 0;
        right: 0;
        position: absolute;

        border: 14rem solid transparent;
        border-top: 14rem solid crimson;
        border-right: 14rem solid crimson;

        transition: borders 1s;
    }

    .left:hover {
        border-width: 16rem;
    }

    .right {
        position: absolute;
        bottom: 0;
        left: 0;

        border: 14rem solid transparent;
        border-bottom: 14rem solid darkmagenta;
        border-left: 14rem solid darkmagenta;

        transition: border-width 1s;
    }

    .right:hover {
        border-width: 16rem;
    }

    .exp, .exp:hover {
        z-index: 2;
        animation: borders 0.8s linear;
        border-top: 19rem solid crimson;
        border-right: 40rem solid crimson;
        border-bottom: 18rem solid crimson;
        border-left: 40rem solid crimson;
    }
</style>