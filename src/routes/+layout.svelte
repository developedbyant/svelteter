
<script lang="ts">
    import "src/assets/app.css"
    import Aside from "src/components/core/aside/Aside.svelte";
    import Nav from "src/components/core/nav/Nav.svelte";
    import TopNav from "src/components/core/nav/TopNav.svelte";
</script>

<div class="layout">
    <Nav />
    <main class="main">
        <TopNav />
        <div class="content">
            <h2>Hello</h2>
        </div>
    </main>
    <Aside />
</div>

<style>
    .layout{
        max-width: var(--maxWidth);
        width: 100%;
        margin: auto;
        display: flex;
        min-height: 100vh;
        background-color: var(--bodyBg);
        color: var(--textColor);
    }
    .main{
        display: flex;
        flex-direction: column;
        width: 100%;
        min-height: 120vh;
        border-right: 2px solid var(--antiBodyBg);
        border-left: 2px solid var(--antiBodyBg);
    }
</style>

