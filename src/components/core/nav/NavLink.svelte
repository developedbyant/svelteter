<script lang="ts">
    import { page } from "$app/stores";
    export let icon:any = undefined
    export let href:string
    /** Indicate if current link is active */
    $: active = href === $page.url.pathname
</script>

<li>
    <a {href} class="navLink" class:active>
        {#if icon}
            <div class="icon">
                <svelte:component this={icon} size="auto"/>
            </div>
        {/if}
        <span class="linkText">
            <slot />
        </span>
    </a>
</li>

<style lang="scss">
    .navLink{
        display: flex;
        align-items: center;
        gap: 10px;
        text-decoration: none;
        color: var(--navColor);
        padding: 10px 15px;
        transition: all ease-in-out 0.4s;
        .linkText{
            font-size: 20px;
            font-weight: 600;
        }
        .icon{
            width: 30px;
            height: auto;
            display: flex;
            align-items: center;
            justify-content: center;
            fill: var(--iconColor);
        }
    }
    .navLink:hover,.navLink.active{
        background-color: var(--antiBodyBg);
        border-radius: 50px;
    }
    // On mobiles
    @media(max-width:700px){
        .navLink{
            padding: 15px;
        }
        .linkText{
            display: none;
        }
    }
</style>