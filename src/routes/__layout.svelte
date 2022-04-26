<div class="header">
    <a class="header-link">Home</a>
    <a class="header-link">About</a>
    <a class="header-link">Photos</a>
    <a class="header-link">Sponsorship</a>
    <a class="header-link">Outreach</a>
</div>

<div class="article-wrapper">
    <article>
        <h1><slot name="title"></slot></h1>
        <slot></slot>
    </article>    
</div>

<style>
	:global(:root) {
		--blue: #1174b7;
		--dark-blue: #0f3e70;
		--light-blue: #00a7d5;
        --off-whtie: #f5f8fa;

		--main-color: var(--blue);
		--secondary-color: var(--dark-blue);
		--alt-color: var(--light-blue);
        --background-color: var(--off-whtie);

        --body-copy: 'Lora', sans-serif;

        --header-height: 5em;
        --content-padding: 1em;
	}

	:global(head, body) {
		width: 100%;
		height: 100%;

        font-family: var(--body-copy);

        background-color: var(--background-color);
	}

	.header {
		position: absolute;
		left: 0;
		top: 0;
		right: 0;
		height: var(--header-height);

		background-color: var(--secondary-color);

        display: flex;
        align-items: center;
        justify-content: center;
	}

    .header-link {
        text-transform: uppercase;
        color: var(--alt-color);
        font-size: 20px;
        font-weight: 900;
        letter-spacing: 0.1em;
        -webkit-font-smoothing: antialiased;

        margin: 1em;
    }

    .header-link:hover {
        border-top: 2px solid #ff000000;
        border-bottom: 2px solid var(--alt-color);
        cursor: pointer;
    }

    .article-wrapper {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;

        margin: var(--content-padding);
        margin-top: calc(var(--header-height) + var(--content-padding));
    }

    article {
        margin: 0 auto;
        max-width: 60em;
        border-radius: 1em;
        padding: 1em;

        border: 1px solid black;
        box-shadow: -6px 6px 8px lightgray;

        background-color: white;
    }
</style>
