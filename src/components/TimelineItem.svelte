<script lang="ts">
    export let time: string;
    export let title: string;
    export let position: string;
    export let href: string;
</script>

<li>
    <time>{time}</time>
    <a {href} target="_blank">{title}</a> - {position}
</li>

<style>
    li {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        column-gap: 0.5rem;
        margin-bottom: 0.5rem;
    }

    time {
        min-width: 75px;
        color: rgb(107 114 128);
    }

    a {
        display: inline-block;
    }
</style>
