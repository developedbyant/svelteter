<script lang="ts">
    import HouseIcon from "src/icons/House.svelte";
    import SearchIcon from "src/icons/Search.svelte"
    import BellIcon from "src/icons/Bell.svelte"
    import EmailIcon from "src/icons/Email.svelte"
    import BookmarksIcon from "src/icons/Bookmark.svelte"
    import ProfileIcon from "src/icons/Person.svelte"
    import NavLink from "./NavLink.svelte";
</script>

<header class="mainHeader">
    <nav class="mainNav">
        <a class="logo" href="/">
            <img src="https://i.ibb.co/9WRfzd1/512px-Logo-of-Twitter-svg.png" alt="twitter">
        </a>
        <ul class="navLinks">
            <NavLink href="/" icon={HouseIcon}>Home</NavLink>
            <NavLink href="/#" icon={SearchIcon}>Explore</NavLink>
            <NavLink href="/#" icon={BellIcon}>Notifications</NavLink>
            <NavLink href="/#" icon={EmailIcon}>Messages</NavLink>
            <NavLink href="/#" icon={BookmarksIcon}>Bookmarks</NavLink>
            <NavLink href="/#" icon={ProfileIcon}>Profile</NavLink>
        </ul>
    </nav>
</header>

<style lang="scss">
    .mainHeader{
        height: 100vh;
        position: sticky;
        left: 0;
        top: 0;
    }
    .mainNav{
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 20px;
        margin-right: 30px;
    }
    .logo{
        display: flex;
        align-items: center;
        justify-content: center;
        width: 40px;
        height: auto;
        margin-bottom: 40px;
        margin-right: auto;
        img{
            object-fit: cover;
            object-position: center;
            width: 100%;
            height: 100%;
        }
    }
    .navLinks{
        display: flex;
        flex-direction: column;
        gap: 15px;
        list-style: none;
        translate: -15px 0;
    }
    // On mobiles
    @media(max-width:700px){
        .logo{
            margin: 0 0 30px 0;
        }
        .navLinks{
            translate: 0 0;
        }
        .mainNav{
            margin: 0px;
        }
    }
</style>