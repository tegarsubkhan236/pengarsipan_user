<script>
    import Footer from "../components/Footer.svelte";
    import Header from "../components/Header.svelte";
    import Sidebar from "../components/Sidebar.svelte";
    import Breadscrumb from "../components/Breadscrumb.svelte";
    import Tree from "../components/Tree.svelte";
    let dataSample = [
        {
            name: "Skripsi",
            counted: 0,
            href: "https://google.com",
            short_desc: "Anuuuu",
            is_opened: false,
            childs: [
                {
                    name: "2018",
                    counted: 0,
                    href: "/s",
                    short_desc: "blah",
                    is_opened: false,
                    items: [
                        {
                            name: "Tegar",
                            counted: 0,
                            href: "/sa",
                            short_desc: "blah",
                            is_opened: false,
                        },
                        {
                            name: "Meysa",
                            counted: 0,
                            href: "/sa",
                            short_desc: "blah",
                            is_opened: false,
                        },
                    ],
                },
            ],
        },
        {
            name: "Skripsi",
            counted: 0,
            href: "https://google.com",
            short_desc: "Anuuuu",
            is_opened: false,
            childs: [
                {
                    name: "2018",
                    counted: 0,
                    href: "/s",
                    short_desc: "blah",
                    is_opened: false,
                    items: [
                        {
                            name: "Tegar",
                            counted: 0,
                            href: "/sa",
                            short_desc: "blah",
                            is_opened: false,
                        },
                        {
                            name: "Meysa",
                            counted: 0,
                            href: "/sa",
                            short_desc: "blah",
                            is_opened: false,
                        },
                    ],
                },
            ],
        },
    ];
</script>

<div id="MathJax_Message" style="display: none;" />
<Header />
<Breadscrumb />
<div class="container" id="main-container">
    <div class="row row-offcanvas row-offcanvas-right">
        <div class="horizontal-slider clearfix">
            <div class="col-xs-12 col-sm-12 col-md-9 main-content">
                <div>
                    <h2 class="ds-div-head page-header first-page-header">
                        Main Collections
                    </h2>
                    <div
                        id="aspect_artifactbrowser_CommunityBrowser_div_comunity-browser"
                        class="ds-static-div primary">
                        <p class="ds-paragraph">
                            Select a main collection to browse its collections.
                        </p>
                        {#each dataSample as data}
                            <Tree config={data} childs={data.childs} />
                        {/each}
                    </div>
                </div>
                <div class="visible-xs visible-sm">
                    <footer>
                        <div class="row">
                            <hr />
                            <div class="col-xs-7 col-sm-8">
                                <div>
                                    Copyright&nbsp;©&nbsp;2020&nbsp;<a
                                        target="_blank"
                                        href="http://perpustakaan.ipb.ac.id">Library</a>
                                    of
                                    <a
                                        target="_blank"
                                        href="https://ipb.ac.id">IPB University</a>
                                    <br />All rights reserved
                                </div>
                                <div class="hidden-print">
                                    <a href="/contact">Contact Us</a>
                                    |
                                    <a href="/feedback">Send Feedback</a>
                                </div>
                            </div>
                            <div class="col-xs-5 col-sm-4 hidden-print">
                                <div class="pull-right">
                                    <span class="theme-by">Indonesia DSpace
                                        Group&nbsp;</span>
                                    <br />
                                    <a href="http://repository.ipb.ac.id/">IPB
                                        University Scientific Repository</a>
                                    <br />
                                    <a
                                        href="http://repository.uinjkt.ac.id/">UIN
                                        Syarif Hidayatullah Institutional
                                        Repository</a>
                                    <br />
                                    <a
                                        href="http://repository.unej.ac.id/">Universitas
                                        Jember Digital Repository</a>
                                    <br />
                                </div>
                            </div>
                        </div>
                        <a class="hidden" href="/htmlmap">&nbsp;&nbsp;</a>
                        <p>&nbsp;</p>
                    </footer>
                </div>
            </div>
            <Sidebar />
        </div>
    </div>
    <div class="hidden-xs hidden-sm">
        <Footer />
    </div>
</div>
