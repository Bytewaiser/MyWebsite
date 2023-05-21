<div class="container">
    <ul>
        <slot />
    </ul>
</div>

<style>
    .container {
        color: var(--color-bg-2);
        min-height: 100vh;
        display: grid;
        align-content: center;
        gap: 2rem;
        padding: 2rem;
        font-family: "Poppins", sans-serif;
    }

    ul {
        --bgColor: rgba(60, 61, 63, 0.7);
        --col-gap: 2rem;
        --row-gap: 2rem;
        --line-w: 0.25rem;
        display: grid;
        grid-template-columns: var(--line-w) 1fr;
        grid-auto-columns: max-content;
        column-gap: var(--col-gap);
        list-style: none;
        width: min(60rem, 95%);
        margin-inline: auto;
    }

    /* line */
    ul::before {
        content: "";
        grid-column: 1;
        grid-row: 1 / span 20;
        background: rgb(32, 32, 32);
        border-radius: calc(var(--line-w) / 2);
    }
    @media (min-width: 40rem) {
        ul {
            grid-template-columns: 1fr var(--line-w) 1fr;
        }
        ul::before {
            grid-column: 2;
        }
    }
</style>
