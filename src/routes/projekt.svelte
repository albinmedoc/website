<script lang="ts">
    import Project from '../components/Project.svelte';

    interface Project {
        project_name: string;
        techniques: string;
        description: string;
        website_url?: string;
        image_url: string;
        bg_color: string;
        header_color: string;
    }

    let projects: Project[] = [
        {
            project_name: 'PlanMan Malmö AB',
            techniques: 'Svelte, Sapper, Node.js, Express',
            description:
                'PlanMan Malmö AB önskade ett sätt att marknadsföra sig mot en bredare publik. Vad passar då bättre än en hemsida? Den presenterar företagets alla tjänster, samt ett formulär för att enkelt ta emot kunders beställningar och frågor.',
            website_url: 'http://www.pmmab.se',
            image_url: '/images/projects/pmmab/preview.png',
            bg_color: '#689caf',
            header_color: '#fff',
        },
        {
            project_name: 'Pamek VVS',
            techniques: 'Svelte, Sapper, Node.js, Express',
            description:
                'Pamek är en nystartad VVS-firma. Hemsidan som skapades åt dem möjliggör för enklare marknadsföring. Deras olika tjänster framgår tydligt, och formuläret på hemsidan gör det enkelt för kunder att ställa frågor och be om offerter.',
            website_url: 'http://www.pamek.nu',
            image_url: '/images/projects/pamek/preview.png',
            bg_color: '#5e5e5e',
            header_color: '#fff',
        },
        {
            project_name: 'The Coffee Lounge',
            techniques: 'Svelte, Sapper, Node.js, Express',
            description:
                'The Coffee Lounge är ett lokalt Café i Staffanstorp. Deras önskemål var att marknadsföra sig över internet. Detta inkluderade skapande av en hemsida, SEO optimering samt hosting och driftsättning. På hemsidan ville dem bland annat att menyn skulle synas & möjlighet till att kunna förbeställa luncher.',
            image_url: '/images/projects/the_coffee_lounge/preview.png',
            bg_color: '#875c2a',
            header_color: '#000',
        },
        {
            project_name: 'Godisbilen',
            techniques: 'Python, Flask',
            description:
                'Godisbilen är ett företag som arbetar i delar av Skåne. Detta företag utför hemleverans av godis under helger. Deras önskemål var att ha en hemsida där man kan beställa hem bilen och därmed handla sitt godis direkt från bilen. Hemsidan inkluderar även att se sortiment, öppettider, information och ett kontaktformulär. När en beställning läggs får kunden direkt en beräknad tid när bilen kommer anlända. Det skapades även ett gränssnitt anpassat för chafförernam för att underlätta deras arbete. Denna visar en karta vart man ska köra, när man ska vara på plats, samt kontaktuppgifter till kunden.',
            image_url: '/images/projects/godisbilen/preview.png',
            bg_color: '#e86ed0',
            header_color: '#b1e8ed',
        },
        {
            project_name: 'Destination Line',
            techniques: 'Python, Flask',
            description:
                'Mitt arbete med Destination Line skedde under deras uppstart. Deras önskemål var att ha en plattform där man kunde dela med sig av sina semesterbilder till allmänheten. Bilderna laddades upp i olika album och hade ett land och stad kopplat till sig. Plattformen tillät även användare att följa varandra och därmed få upp deras album i flödet. En sökfunktion skapades för att söka efter både personer, land och stad.',
            image_url: '/images/projects/destination_line/preview.png',
            bg_color: '#4fadec',
            header_color: '#d4aa5f',
        },
    ];
</script>

<style>
    #work {
        max-width: none;
        padding: 40px 20px;
        margin: 100px 0 0 0;
        text-align: center;
        color: #f52735;;
    }

    #work > img {
        width: 200px;
    }

    #work > h2 {
        font-size: 2em;
    }

    #work > p {
        max-width: 400px;
        margin: 0 auto;
        color: #000;
    }

    #work > p > a {
        color: #f52735;
    }
</style>

<section id="work">
    <img src="/images/iMac.svg" alt="computer"/>
    <h2>Mina senaste projekt</h2>
    <p>
        Här är några av mina senaste projekt, besök min
        <a
            href="https://github.com/albinmedoc?tab=repositories"
            target="_blank">
            GitHub-profil
        </a>
        för att se fler.
    </p>
</section>
<div id="projects">
    {#each projects as project}
        <Project {...project} />
    {/each}
</div>
