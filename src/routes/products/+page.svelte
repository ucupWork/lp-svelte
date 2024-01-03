c<script>
    import Navbar from "../../lib/components/navbar.svelte";
    import Footer from "../../lib/components/footer.svelte";
    import Slider from "../../lib/components/products/slider.svelte"
    import ConsultBanner from "../../lib/components/consultation-banner/banner.svelte";
    import AgentBanner from "../../lib/components/agent-banner/banner.svelte";
</script>
<Navbar/>
<div class="grid grid-cols-1 lg:grid-cols-2">
<ConsultBanner/>
<AgentBanner/>
</div>
<Slider/>
<Footer/>