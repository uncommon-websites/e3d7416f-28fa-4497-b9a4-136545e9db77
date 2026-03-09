<script lang="ts">
	import "../app.css";
    import Header from "$lib/components/Header.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<div class="min-h-screen bg-white font-sans text-gray-900 selection:bg-[#0ea5e9]/20 selection:text-black">
    <Header />
    <slot />
    <Footer />
</div>
