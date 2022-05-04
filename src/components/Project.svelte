<script lang="ts">
    export let project_name: string;
    export let techniques: string;
    export let description: string;
    export let website_url: string = undefined;
    export let image_url: string;
    export let bg_color: string;
    export let header_color: string;
</script>

<style>
    .project{
        background-color: var(--bg-color);
    }
    .project > .container {
        margin: 0 auto;
        max-width: 1000px;
        width: calc(100% - 40px);
        padding: 40px 20px;
        margin: 0 auto;
        text-align: center;
    }

    .project > .container > img {
        margin: 0 auto;
        width: 80%;
        max-width: 800px;
    }

    .project > .container > .project_name {
        font-size: 45px;
        margin: 0;
        color: var(--header-color);
    }

    .project > .container > .project_name > a {
        color: var(--header-color);
    }
</style>

<section class="project" style="--bg-color: {bg_color}; --header-color: {header_color}">
    <div class="container">
        <img src={image_url} width="1000px" alt={project_name} />
        <h3 class="project_name">
            {#if website_url}
                <a href="{website_url}" target="_blank">{project_name}</a>
            {:else}
                {project_name}
            {/if}
        </h3>
        <p class="tags" style="color: #fff;">{techniques}</p>
        <p class="description" style="color: #fff;">{description}</p>
    </div>
</section>
