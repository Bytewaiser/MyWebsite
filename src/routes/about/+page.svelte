<script>
    import TimelineItem from "../../components/TimelineItem.svelte";
</script>

<svelte:head>
    <title>About - Hasan Hüseyin Yurdagül</title>
    <meta name="description" content="About Hasan Hüseyin Yurdagül" />
</svelte:head>

<style>
h2 {
    margin-bottom: 1rem;
    font-size: x-large; 
    font-weight: bold;
}

</style>

<div class="text-column">
    <h1>About Me</h1>
    <section aria-label="Timeline list">
        <h2>Work Timeline</h2>
        <p>This is my work history, some of them I still work some of them not. </p>
        <ul>
            <TimelineItem
                time="2022-01"
                title="Datakod"
                position="R&D Center Consultant"
                href="https://www.datakod.com/"
            />
            <TimelineItem
                time="2022-01"
                title="Kolaybi"
                position="R&D Center Consultant"
                href="https://www.kolaybi.com/"
            />
            <TimelineItem
                time="2022-01"
                title="NanoWorks"
                position="R&D Center Consultant"
                href="https://nano.eu.com/"
            />
            <TimelineItem
                time="2021-10"
                title="Synapsis"
                position="Data Science Consultant"
                href="https://synapsis.com.tr/"
            />
            <TimelineItem
                time="2021-09"
                title="UGM"
                position="Lead Machine Learning Engineer"
                href="https://ugm.com.tr"
            />
            <TimelineItem
                time="2021-09"
                title="HepsiEmlak"
                position="R&D Center Consultant"
                href="https://www.hepsiemlak.com/"
            />
            <TimelineItem
                time="2021-08"
                title="Protel"
                position="Data Science Consultant"
                href="https://www.protel.com.tr/"
            />
            <TimelineItem
                time="2021-05"
                title="OxyAI"
                position="Lead Machine Learning Engineer"
                href="http://www.oxyai.com"
            />
            <TimelineItem
                time="2021-04"
                title="Universal"
                position="Lead Research Scientist"
                href="https://www.uni-yaz.com"
            />
            <TimelineItem
                time="2021-04"
                title="Albert Solino"
                position="R&D Center Consultant"
                href="https://www.albertsolino.com/"
            />
            <TimelineItem
                time="2020-12"
                title="Smartiks"
                position="Data Science Consultant"
                href="https://www.smartiks.com.tr/"
            />
            <TimelineItem
                time="2020-08"
                title="Technorot"
                position="Data Science Consultant"
                href="https://www.teknorot.com/"
            />
            <TimelineItem
                time="2020-08"
                title="Sefamerve"
                position="Data Science Consultant"
                href="https://www.sefamerve.com/"
            />
            <TimelineItem
                time="2020-05"
                title="Comdata"
                position="R&D Center Consultant"
                href="https://www.comdatagroup.com/"
            />
            <TimelineItem
                time="2020-05"
                title="Gtech"
                position="Data Science Consultant"
                href="https://www.gtech.com.tr/en/"
            />
        </ul>
    </section>
</div>
