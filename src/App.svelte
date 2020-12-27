<script>
    import { Router, Route, Link } from 'svelte-routing';
    export let url = '';

    import Header from './Header.svelte';
    import Footer from './Footer.svelte';

    // Import pages
    import NotFound from './pages/NotFound.svelte';
    import Home from './pages/home/index.svelte';
    import Contact from './pages/contact/index.svelte';
    import Projects from './pages/projects/index.svelte';
</script>

<style>
</style>

<Router {url}>
    <Header/>
    <main>
        <!-- Setup pages -->
        <Route component={NotFound} />
        <Route path="/" component={Home} />
        <Route path="/projekt" component={Projects} />
        <Route path="/kontakt" component={Contact} />
    </main>
    <Footer/>
</Router>
