<script>
    import * as config from '$lib/config'
</script>

<nav>
    <a href="/" class="title">
        <b>{config.title}</b>
    </a>

    <ul class="links">
        <li>
            <a href="/about">READ</a>
        </li>
        <li>
            <a href="/contact">ABOUT</a>
        </li>
    </ul>

    <button>Contact</button>
</nav>

<style>
    nav {
        font-family: 'Silkscreen', system-ui;
        color: #FCCC8E;
        padding-block: 2rem
    }

    .links {
        margin-block: 3rem;
    }

    ul {
        list-style-type: none;
    }


    a {
        font-size: 1rem;
        /* color: #FCCC8E; */
        text-decoration: none;
    }

    b {
        font-size: 1rem;
    }

    @media (min-width: 768px) {
        nav {
            display: flex;
            justify-content: space-between;
        }

        .links {
            display: flex;
            gap: 1rem;
            margin-block: 0;
        }
    }
</style>