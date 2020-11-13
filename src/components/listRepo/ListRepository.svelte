<script>
    export let title,
        author_name = [],
        short_desc = "",
        published_date = "",
        is_odd = false,
        href = "";
</script>

<li class="ds-artifact-item {is_odd ? 'odd' : 'even'}">
    <div class="artifact-description">
        <h4 class="artifact-title">
            <a {href}>{title}</a><span class="Z3988" />
        </h4>
        <div class="artifact-info">
            <span class="author h4">
                <small>
                    {#each author_name as name}<span>{name} | </span>{/each}
                </small>
            </span>
            <span class="publisher-date h4">
                <small><span>{published_date}</span></small>
            </span>
        </div>
        <div class="artifact-abstract">{short_desc}</div>
    </div>
</li>
