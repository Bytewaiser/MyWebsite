<script lang="ts">
    export let date: string;
    export let title: string;
    export let position: string;
    export let href: string;
</script>

<li>
    <div class="date">{date}</div>
    <div class="title"><a {href} target="_blank">{title}</a> - {position}</div>
    <div class="descr">
        Description will come!!!
    </div>
</li>

<style>
    /* row gaps */
    li:not(:last-child) {
        margin-bottom: var(--row-gap);
    }

    /* card */
    li {
        --accent-color: #300;
        grid-column: 2;
        --inlineP: 1.5rem;
        margin-inline: var(--inlineP);
        grid-row: span 2;
        display: grid;
        grid-template-rows: min-content min-content min-content;
    }

    /* date */
    li .date {
        --dateH: 3rem;
        height: var(--dateH);
        margin-inline: calc(var(--inlineP) * -1);

        text-align: center;
        background-color: var(--accent-color);

        color: white;
        font-size: 1.25rem;
        font-weight: 700;

        display: grid;
        place-content: center;
        position: relative;

        border-radius: calc(var(--dateH) / 2) 0 0 calc(var(--dateH) / 2);
    }

    /* date flap */
    li .date::before {
        content: "";
        width: var(--inlineP);
        aspect-ratio: 1;
        background: var(--accent-color);
        background-image: linear-gradient(rgba(0, 0, 0, 0.2) 100%, transparent);
        position: absolute;
        top: 100%;

        clip-path: polygon(0 0, 100% 0, 0 100%);
        right: 0;
    }

    /* circle */
    li .date::after {
        content: "";
        position: absolute;
        width: 2rem;
        aspect-ratio: 1;
        background: var(--bgColor);
        border: 0.3rem solid var(--accent-color);
        border-radius: 50%;
        top: 50%;

        transform: translate(50%, -50%);
        right: calc(100% + var(--col-gap) + var(--line-w) / 2);
    }

    /* title descr */
    li .title,
    li .descr {
        background: var(--bgColor);
        position: relative;
        padding-inline: 1.5rem;
    }
    li .title {
        overflow: hidden;
        padding-block-start: 1.5rem;
        padding-block-end: 1rem;
        font-weight: 500;
    }
    li .descr {
        padding-block-end: 1.5rem;
        font-weight: 300;
        border-bottom-right-radius: 1rem;
        border-bottom-left-radius: 1rem;
    }

    /* shadows */
    li .title::before,
    li .descr::before {
        content: "";
        position: absolute;
        width: 90%;
        height: 0.5rem;
        background: rgba(0, 0, 0, 0.5);
        left: 50%;
        border-radius: 50%;
        filter: blur(4px);
        transform: translate(-50%, 50%);
    }
    li .title::before {
        bottom: calc(100% + 0.125rem);
    }

    li .descr::before {
        z-index: -1;
        bottom: 0.25rem;
    }

    @media (min-width: 40rem) {
        li:nth-child(odd) {
            grid-column: 1;
        }
        li:nth-child(even) {
            grid-column: 3;
        }

        /* start second card */
        li:nth-child(2) {
            grid-row: 2/4;
        }

        li:nth-child(odd) .date::before {
            clip-path: polygon(0 0, 100% 0, 100% 100%);
            left: 0;
        }

        li:nth-child(odd) .date::after {
            transform: translate(-50%, -50%);
            left: calc(100% + var(--col-gap) + var(--line-w) / 2);
        }
        li:nth-child(odd) .date {
            border-radius: 0 calc(var(--dateH) / 2) calc(var(--dateH) / 2) 0;
        }
    }
</style>
