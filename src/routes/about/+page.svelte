<script>
    import TimelineItem from "../../components/TimelineItem.svelte";
    import TimelineContainer from "../../components/TimelineContainer.svelte";
    let data = [
        {
            date: "2023 Jan - Present",
            title: "Smartiks",
            position: "Machine Learning Engineer",
            href: "https://www.smartiks.com.tr/",
        },
        {
            date: "2021 Apr - Present",
            title: "Universal",
            position: "Lead Research Scientist",
            href: "https://www.uni-yaz.com",
        },
        {
            date: "2022 Jan - Present",
            title: "Datakod",
            position: "R&D Center Consultant",
            href: "https://www.datakod.com/",
        },
        {
            date: "2022 Jan - Present",
            title: "Kolaybi",
            position: "R&D Center Consultant",
            href: "https://www.kolaybi.com/",
        },
        {
            date: "2022 Jan - Present",
            title: "NanoWorks",
            position: "R&D Center Consultant",
            href: "https://nano.eu.com/",
        },
        {
            date: "2021 Nov - Present",
            title: "Synapsis",
            position: "Data Science Consultant",
            href: "https://synapsis.com.tr/",
        },
        {
            date: "2021 Apr - Present",
            title: "Albert Solino",
            position: "R&D Center Consultant",
            href: "https://www.albertsolino.com/",
        },
        {
            date: "2021 May - 2023 Jan",
            title: "OxyAI",
            position: "Lead Machine Learning Engineer",
            href: "http://www.oxyai.com",
        },
        {
            date: "2020 Sep - 2023 Jan",
            title: "Smartiks",
            position: "Data Science Consultant",
            href: "https://www.smartiks.com.tr/",
        },
        {
            date: "2021 Sep - 2022 Oct",
            title: "UGM",
            position: "Lead Machine Learning Engineer",
            href: "https://ugm.com.tr",
        },
        {
            date: "2021 Sep - 2022 May",
            title: "HepsiEmlak",
            position: "R&D Center Consultant",
            href: "https://www.hepsiemlak.com/",
        },
        {
            date: "2021 Aug - 2022 Apr",
            title: "Protel",
            position: "Data Science Consultant",
            href: "https://www.protel.com.tr/",
        },
        {
            date: "2020 Aug - 2021 Nov",
            title: "Technorot",
            position: "Data Science Consultant",
            href: "https://www.teknorot.com/",
        },
        {
            date: "2020 Aug - 2021 Oct",
            title: "Sefamerve",
            position: "Data Science Consultant",
            href: "https://www.sefamerve.com/",
        },
        {
            date: "2020 May - 2021 Sep",
            title: "Comdata",
            position: "R&D Center Consultant",
            href: "https://www.comdatagroup.com/",
        },
        {
            date: "2020 May - 2021 Sep",
            title: "Gtech",
            position: "Data Science Consultant",
            href: "https://www.gtech.com.tr/en/",
        },
    ];
</script>

<svelte:head>
    <title>About - Hasan Hüseyin Yurdagül</title>
    <meta name="description" content="About Hasan Hüseyin Yurdagül" />
</svelte:head>

<div class="text-column">
    <h1>About Me</h1>
    <section aria-label="Timeline list">
        <h2>Work Timeline</h2>
        <p>
            This is my work history, some of them I still work some of them not.
        </p>
        <TimelineContainer>
            {#each data as { date, title, position, href }}
                <TimelineItem {date} {title} {position} {href} />
            {/each}
        </TimelineContainer>
    </section>
</div>

<style>
    h2 {
        margin-bottom: 1rem;
        font-size: x-large;
        font-weight: bold;
    }
</style>
