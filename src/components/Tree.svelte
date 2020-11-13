<script>
    export let config = {
        name: null,
        counted: 0,
        href: null,
        short_desc: null,
        is_opened: false,
    };
    export let childs = [
        {
            name: "Sample",
            counted: 0,
            href: null,
            short_desc: null,
            is_opened: false,
            items: [
                {
                    name: null,
                    counted: 0,
                    href: null,
                    short_desc: null,
                    is_opened: false,
                },
            ],
        },
    ];
    export let is_opened = false;
</script>

<div
    id="aspect_artifactbrowser_CommunityBrowser_referenceSet_community-browser"
    class="ds-static-div community-browser-wrapper">
    <div class="ds-static-div row community-browser-row">
        <div class="ds-static-div col-xs-2 col-sm-1">
            <p class="toggler-wrap">
                <a
                    role="button"
                    on:click={() => (is_opened = !is_opened)}
                    href="#"
                    class="btn btn-default btn-sm toggler collapsed"><i
                        aria-hidden="true"
                        class="glyphicon glyphicon-minus open-icon {!is_opened ? 'hidden' : null}" /><i
                        aria-hidden="true"
                        class="glyphicon glyphicon-plus closed-icon {is_opened ? 'hidden' : null}" /></a>
            </p>
        </div>
        <div class="ds-static-div col-xs-10 col-sm-11">
            <a
                href={config.href}
                name="community-browser-link">{config.name}</a>
            [{config.counted}]
        </div>
        <div class="ds-static-div sub-tree-wrapper">
            {#each childs as child}
                <div
                    class="{!is_opened ? 'hidden' : null} ds-static-div row community-browser-row open-community-browser-row current-community-browser-row">
                    <div
                        class="ds-static-div col-xs-2 col-sm-1 col-sm-offset-1">
                        <p class="toggler-wrap">
                            <a
                                data-target="#collapse-123456789_27"
                                role="button"
                                on:click={() => (child.is_opened = !child.is_opened)}
                                href="#"
                                class="btn btn-default btn-sm toggler collapsed"><strong><i
                                        aria-hidden="true"
                                        class="glyphicon glyphicon-minus open-icon {!child.is_opened ? 'hidden' : null}" /><i
                                        aria-hidden="true"
                                        class="glyphicon glyphicon-plus closed-icon {child.is_opened ? 'hidden' : null}" /></strong></a>
                        </p>
                    </div>
                    <div class="ds-static-div col-xs-10 col-sm-10">
                        <a
                            href={child.href}
                            name="community-browser-link"><strong>{child.name}</strong></a>
                        [{child.counted}]

                        <p class="ds-paragraph hidden-xs">{child.short_desc}</p>
                    </div>
                </div>
                {#each child.items as myItem}
                    <div
                        class="{!child.is_opened ? 'hidden' : null} {!is_opened ? 'hidden' : null} ds-static-div sub-tree-wrapper">
                        <div class="ds-static-div row community-browser-row">
                            <div
                                class="ds-static-div col-xs-10 col-sm-9 col-sm-offset-3 col-xs-offset-2">
                                <a
                                    href={myItem.href}
                                    name="community-browser-link">{myItem.name}</a>
                                [{myItem.counted}]
                            </div>
                        </div>
                    </div>
                {/each}
            {/each}
        </div>
    </div>
</div>
