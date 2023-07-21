<script lang="ts">
</script>

<aside>
    <div class="test">
        <h3>Get Verified</h3>
        <p>Subscribe to unlock new features.</p>
        <button>Get Verified</button>
    </div>
</aside>

<style lang="scss">
    aside{
        height: 100vh;
        min-width: 300px;
        margin-left: 30px;
        position: sticky;
        width: fit-content;
        padding: 10px;
        top: 0;
        right: 0;
    }
    .test{
        display: flex;
        flex-direction: column;
        gap: 5px;
        background-color: var(--antiBodyBg);
        padding: 10px;
        border-radius: 5px;
        overflow: hidden;
    }
    .test button{
        padding: 10px 20px;
        border-radius: 20px;
        border: none;
        font-size: 14px;
        font-weight: 600;
        width: fit-content;
        background-color: var(--buttonBg);
        color: var(--buttonColor);
    }
</style>