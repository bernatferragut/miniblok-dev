<script>
    import * as config from '$lib/config'
    export const prerender = true
</script>

<nav>
    <a href="https://miniblok.surge.sh/" class="title">
        <b>{config.title}</b>
    </a>

    <ul class="links">
        <li>
            <a href="/about">ABOUT</a>
        </li>
        <li>
            <a href="/contact" class="mail">CONTACT</a>
        </li>
    </ul>

</nav>

<style>
    nav {
        font-family: 'Silkscreen', system-ui;
        color: #FCCC8E;
        padding-block: 1rem ;
        border-bottom: 1px solid;
    }
    
    .links {
        margin-block: 3rem;
    }

    ul {
        list-style-type: none;
    }


    a {
        font-size: 1rem;
        text-decoration-color: inherit;
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