<script>
    import * as config from '$lib/config'
    import '@fontsource/silkscreen';
</script>

<footer>
    <p>{config.title} &copy {new Date().getFullYear()}</p> 
</footer>


<style>
    footer {
        font-family: 'Silkscreen', system-ui;
        color: #FCCC8E;
        padding-block: 50px ;
        border-top: 1px solid;
    }

    p {
        color: #FCCC8E;
        font-size: 0.9rem;
    }

</style>