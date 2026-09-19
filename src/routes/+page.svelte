<script>
    import ProjectCard from '$lib/ProjectCard.svelte';
	// import { title } from 'process';
    const projects = [
        {title: "epilogue.",
        category: "Interactive Data Storytelling",
        desc: "I created this interactive 'scrollytelling' website with Svelte, using real-world data from the Black Wealth Data Center to narratively explore the Great Migration. My goal was to combine interactive visualization and responsive web design with my passion for telling stories. For this project, I was selected as a finalist in the Bloomberg-sponsored Kode With Klossy x BWDC Data Scrollytelling challenge in the 'Can't Put It Down' category, honored specifically for my narrative storytelling.",
        image: '/images/bwdc.png',
        imageAlt: "Screenshot of the 'epilogue.' webpage header",
        link: 'https://maggiechristoffersen.github.io/data-storytelling/',
        linkText: 'Explore the narrative',
        tools: ['Svelte', 'JavaScript', 'Data visualization', 'Tableau', 'Scrollytelling']},
        // FP Project goes here...
    ];
    const data_stories = [
        {
            title: 'Speech, controversy and freedom at UMich',
            category: 'Data Journalism',
            publication: 'The Michigan Daily',
            date: 'March 26, 2026',
            desc: 'In this collaborative story, I explored aggregate data from the FIRE College Free Speech survey to report on trends in campus environment and first amendment-related issues particular to the University of Michigan and the state of Michigan as a whole. The story is data-driven and framed by demographic and ideological differences between higher-education institutions in Michigan.',
            image: '/images/speech-graphic.png',
            link: 'https://www.michigandaily.com/web/data/speech-controversy-and-freedom-at-umich/',
            linkText: 'Read the story',
            tools: ['Python', 'Data reporting', 'Visualization', 'Datawrapper']
        },
        {
            title: 'The Statement 2025 Sex Survey',
            category: 'Data Journalism',
            publication: 'The Michigan Daily',
            date: 'December 9, 2025',
            desc: "I collaborated with The Michigan Daily's long-form magazine The Statement to perform data analysis on their annual sex survey and create graphics for the piece.",
            image: '/images/sex-survey.png',
            link: 'https://www.michigandaily.com/statement/the-statement-2025-sex-survey/',
            linkText: 'Check out the results',
            tools: ['Python', 'Visualization', 'Data analysis', 'Datawrapper']
        }
    ];
    const culture_stories = [
        {
            title: "TikTok Tarot Readings: Invites to self-reflection or attention grabs?",
            category: "Culture Reporting",
            publication: "Her Campus at U Mich",
            date: "April 11, 2026",
            desc: "I reported this digital-culture feature examining the trend of Tarot readings hosted on TikTok, interviewing a U-M professor to connect the phenomenon to black-box algorithms and young-adult mental health.",
            image: '/images/tarot_cards_by_Viva_Luna_Studios.webp',
            imageAlt: 'Cover image depicting tarot cards',
            link: 'https://www.hercampus.com/school/u-mich/tiktok-tarot-readings-invites-to-self-reflection-or-attention-grabs/',
            linkText: 'Read the article',
            tools: ['Interviewing', 'Culture reporting', 'Digital content']
        }
    ];
    const current_projects = [
        {
            title: "What German society understands about data privacy that American lawmakers don't",
            type: "German Honors Thesis",
            status: "In Progress",
            expected: "Expected April 2027",
            desc: "A comparative study of the sociopolitical and cultural factors to the perception of data privacy in the American compared to that of Germany, with attention to Datenschutz and legislation and policy implementations in Germany and the broader European Union.",
            methods: ['Comparative policy analysis', 'German-language research', 'Privacy and information governance']
        },
        {
            title: "Data Science for Legal Justice in the Wayne County Court System",
            type: "Data Science Capstone Project",
            status: "In Progress",
            expected: "Expected December 2026",
            desc: "An applied data science project examining data in the Wayne County Court system by way of building a web scraper, employing a SQL database, and utilizing Python libraries for data analysis.",
            methods: ['Data analysis', 'Legal and institutional research', 'Ethics in data use']
        },
        {
            title: "Web History and Internet Research Lab",
            type: "Digital Studies Institute Research",
            status: 'In Progress',
            expected: '',
            desc: "I perform research on queer and marginalized histories of the internet, focusing on questions of digital community, visibility, memory, and preservation.",
            methods: ['Archival research', 'Internet history', 'Digital culture']
        }
    ] // idk how i exactly will format this
</script>

<svelte:head>
    <title>Maggie Christoffersen | Data Journalist & Interactive Storyteller</title>
</svelte:head>

<header class="site-header">
    <a class="site-name" href="#top">Maggie Christoffersen</a>

    <nav aria-label="Main navigation">
        <a href="#interactive">Interactive</a>
        <a href="#data">Data</a>
		<a href="#culture">Culture</a>
		<a href="#current">Current Projects</a>
		<a href="#about">About</a>
    </nav>
</header>
<main id="main-content">
    <section class="hero" id="top">
        <p class="eyebrow">Data Journalist | Interactive Storyteller | Digital Editor</p>
        <h1>I report, analyze, and build stories about technology and public life.</h1>
        <p class="hero-copy">I am a University of Michigan senior studying Data Science and German, minoring in Science, Technology, and Society. My work combines reporting, data analysis, visualization, and web development to examine technology, data privacy, legal justice, and digital culture.</p>
        <div class="hero-links">
            <a class="button primary-button" href="#interactive">
                Check out my work
            </a>
            <a class="button secondary-button" href="/resume.pdf">
                View my resume
            </a>
        </div>
    </section>
    <section class="work-section" id="interactive">
        <div class="section-heading">
            <p class="eyebrow"> Selected Projects </p>
            <h2> Interactives & Graphics </h2> 
            <p>
                Graphic components, scrollytelling, and front-end projects developed with the goal of making information accessible.
            </p>
        </div>
        <div class="project-grid">
            {#each projects as project}
                <ProjectCard {...project}/>
            {/each}
        </div>
    </section>
    <section class="work-section alternate" id="data">
        <div class="section-heading">
            <p class="eyebrow">Data Journalism</p>
            <h2>Data Journalism</h2>
            <p> My reporting using data analysis, visualization, and document research. </p>
        </div>
        <div class="project-grid">
            {#each data_stories as project}
                <ProjectCard {...project}/>
            {/each}
        </div>
    </section>
            <section class="work-section" id="culture">
        <div class="section-heading">
            <p class="eyebrow">Writing and Editing</p>
            <h2>Culture, Media, & Editorial Work</h2>
            <p> I write on digital culture and examine how online phenomena shape our lives through cultural criticism and editorial work. </p>
        </div>
        <div class="project-grid">
            {#each culture_stories as project}
                <ProjectCard {...project}/>
            {/each}
        </div>
    </section>
    <section class="research-section" id="research">
        {#each current_projects as project}
            <article class="research-card">
                <div class="status-row">
                    <span class="status">
                        {project.status}
                    </span>
                    {#if project.expected}
                        <span class="expected">
                            {project.expected}
                        </span>
                    {/if}
                </div>
                <p class="project-category">
                    {project.type}
                </p>
                <h3>{project.title}</h3>
                <p>{project.desc}</p>
                <ul class="tag-list" aria-label="Methods and Topics">
                    {#each project.methods as method}
                        <li>{method}</li>
                    {/each}
                </ul>
            </article>
        {/each}
    </section>
    <section class="about-section" id="about">
        <div>
            <p class="eyebrow">
                About Me
            </p>
            <h2>Journalism informed by data, history, and culture</h2>
        </div>
        <div class="about-copy">
            <p>
                I'm a data journalist and digital editor at the University of Michigan. I serve as the Editor-in-Chief of Her Campus at U Mich, an online campus magazine, and work on The Michigan Daily's web team as a data journalist (and formerly, the Managing Online Editor). 
            </p>
            <p>
                My academic work is in many departments: I am majoring in both Data Science and German, and minoring in Science, Technology, and Society. I also do research for the University's Digital Studies Institute. This informs my reporting interests in privacy, surveillance, digital culture, legal systems, and marginalized online communities.
            </p>
            <p>
                I work with Python, R, SQL, Svelte, and JavaScript (React and Vue). I am fluent in German.
            </p>
            <div class="contact-links">
                <a href="mailto:maggierc@umich.edu">Email me</a>
                <a href="https://www.linkedin.com/in/maggiechris/">LinkedIn</a>
                <a href="/resume.pdf">Resume</a>
            </div>
        </div>
    </section>
</main>

<footer>Designed and developed by Maggie Christoffersen. Built with Svelte.</footer>
