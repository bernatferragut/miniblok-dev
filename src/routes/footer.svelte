<script>
    import * as config from '$lib/config'
    import '@fontsource/silkscreen';
</script>

<footer>
    <p>{config.title} &copy {new Date().getFullYear()}</p> 
    <ul class="links">
        <li>
            <a href="https://linktr.ee/bernatferragutsole">linktree</a>
        </li>
    </ul>
</footer>


<style>
    footer {
        font-family: 'Silkscreen', system-ui;
        padding-block: 1rem ;
        border-top: 1px solid;
        display: flex;
        justify-content: space-between;
        
    }

    .links {
            display: flex;
            gap: 1rem;
            margin-block: 0;
        }

     a {
        font-size: 1rem;
        text-decoration-color: inherit;
    }

    ul {
        list-style-type: none;
    }

    p {
        color: #FCCC8E;
        font-size: 0.9rem;
    }

</style>
