<script>
    import avatar from "$lib/images/avatar.jpg";
    import TwitterIcon from "../components/icons/TwitterIcon.svelte";
    import GithubIcon from "../components/icons/GithubIcon.svelte";
    import LinkedinIcon from "../components/icons/LinkedinIcon.svelte";
</script>

<svelte:head>
    <title>Home - Hasan Hüseyin Yurdagül</title>
    <meta
        name="description"
        content="Hasan Hüseyin Yurdagül Personal Website"
    />
</svelte:head>

<section>
    <img src={avatar} alt="Photo of Hasan Hüseyin Yurdagül" />
    <h1>Hasan Hüseyin Yurdagül</h1>
    <p>
        Hi, I am Hasan, I am a <b>Senior Machine Learning Engineer</b> at
        <a href="https://uni-yaz.com" target="_blank">Universal Software</a> and
        <a href="https://smartiks.com.tr" target="_blank">Smartiks Software</a>.
    </p>
    <div class="contact">
        <p>Reach me at:</p>
        <div>
            <a href="https://www.linkedin.com/in/bytewaiser/" target="_blank">
                <LinkedinIcon />
            </a>
            <a href="https://github.com/bytewaiser" target="_blank">
                <GithubIcon />
            </a>
            <a href="https://twitter.com/hasanhyurdagul" target="_blank">
                <TwitterIcon />
            </a>
        </div>
    </div>
</section>

<style>
    .contact {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .contact a {
        margin-left: 5px;
        margin-right: 5px;
    }
    img {
        width: 100px;
        border-radius: 50%;
        margin-bottom: -20px;
    }
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        flex: 0.5;
    }
</style>
