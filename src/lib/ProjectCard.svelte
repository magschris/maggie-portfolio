<script>
    let {
        title, 
        desc, 
        category, 
        publication = '',
        date = '',
        image = '',
        imageAlt = '',
		link = '',
		linkText = 'Take me there',
		tools = []
    } = $props();
</script>

<article class="proj-card">
    {#if image}
        <img
            class = "proj-image"
            src={image}
            alt={imageAlt}
            loading="lazy" 
        />
    {/if}
    <div class="proj-content">
        <p class="proj-category">{category}</p>
        <h3>{title}</h3>
        {#if publication || date}
            <p class="proj-meta">
                {publication}
                {#if publication && date}
                    <span aria-hidden="true"> | </span>
                {/if}
                {date}
            </p>
        {/if}
        <p>{desc}</p>
        {#if tools.length}
            <ul class="tag-list" aria-label="Tools I Used">
                {#each tools as tool}
                    <li>{tool}</li>
                {/each}
            </ul>
        {/if}
        {#if link}
            <a class="proj-link" href={link}>
                {linkText}
                <span aria-hidden="true"> → </span>
            </a>
        {/if}
    </div>
</article>