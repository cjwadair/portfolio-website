<script lang="ts">
  import ProjectCard from '../components/ProjectCard.svelte';
  import Badge from '../components/Badge.svelte';
</script>

<div class="px-20 py-16">

  <section class="pt-20 pb-48">
    <div class="flex gap-x-20">
      
      <div class="w-1/2">
        <div class="flex gap-x-8"> 

          <div>
            <img src="/IMG_0905.jpg" alt="Chris Adair" class="rounded-full w-36 h-36 object-cover border-2 border-slate-300 shadow-lg"/>
          </div>
          
          <div class="flex flex-col justify-center">
            <p class="px-2">Hello! I'm</p>
            <p class="text-8xl text-left">Chris Adair</p>
            <div class="px-2 flex">Full Stack Developer <span class="px-1">&#8226;</span> Toronto, Ontario. <span class="px-1">&#8226;</span> <a href="https://github.com/cjwadair" class="iconify devicon--github h-6 w-6"></a> <span class="px-1">&#8226;</span> <a href="http://www.linkedin.com/in/chris-adair-5740982" class="iconify devicon-plain--linkedin h-6 w-6"></a>
            </div>
          </div>

        </div>
        
        <p class="mt-8">Results-driven Full Stack Software Developer with extensive experience designing, building, and maintaining intuitive web applications. Proven expertise in leading development projects, integrating external APIs, and delivering scalable, maintainable solutions that enhance functionality and improve user experience. Adept at collaborating with stakeholders to deliver value-driven technology in fast-paced environments.</p>
      </div>
    </div>
  </section>

  <section class="w-2/3 pb-48">
    
    <h2 class="text-4xl pb-2 border-b border-slate-300">Tech Stack</h2>
    
    <div class="pt-12">
      <p class="text-xl">Primary</p>
      <div class="flex flex-wrap gap-3 mt-2">
        <!-- {#each ['Ruby on Rails', 'PostgreSQL', 'JavaScript (ES6+)', 'Hotwire', 'Stimulus', 'TailwindCSS', 'Rspec', 'Github', 'Heroku', 'Memcached', 'Redis'] as skill} -->
        {#each [
          { label: 'Ruby on Rails', iconName: 'rails' },
          { label: 'PostgreSQL', iconName: 'postgresql' },
          { label: 'JavaScript (ES6+)', iconName: 'javascript' },
          { label: 'Heroku', iconName: 'heroku' },
          { label: 'TailwindCSS', iconName: 'tailwindcss' },
          { label: 'Hotwire', iconName: 'hotwire' },
          { label: 'Stimulus', iconName: 'stimulus' },
          { label: 'Rspec', iconName: 'rspec' },
          { label: 'Github', iconName: 'github' },
          { label: 'Memcached', iconName: 'memcached' },
          { label: 'Redis', iconName: 'redis' }
        ] as skill}
          <Badge label={skill.label} icon={skill.iconName} />
        {/each}
        
        </div>
    </div>
    
    <div class="pt-12">
      <p class="text-xl">Familiar With</p>
      <ul class="flex flex-wrap gap-3 mt-2">
        <!-- {#each ['Python', 'Go', 'Node', 'Typescript', 'React', 'Vue', 'Svelte', 'Docker', 'Figma', 'Sketch'] as skill} -->
        {#each [
          { label: 'Python', iconName: 'python' },
          { label: 'Go', iconName: 'go' },
          { label: 'Node', iconName: 'nodejs' },
          { label: 'Typscript', iconName: 'typescript' },
          { label: 'React', iconName: 'react' },
          { label: 'Vue', iconName: 'vuejs' },
          { label: 'Svelte', iconName: 'svelte' },
          { label: 'Docker', iconName: 'docker' },
          { label: 'Postman', iconName: 'postman' },
          { label: 'SQLite', iconName: 'sqlite' },
          { label: 'Elasticsearch', iconName: 'elasticsearch' },
          { label: 'Figma', iconName: 'figma' },
          { label: 'Sketch', iconName: 'sketch' }
        ] as skill}
          <Badge label={skill.label} icon={skill.iconName} />
        {/each}

      </ul>
    </div>

  </section>

  <section class="w-2/3 pb-48">

      <h2 class="text-3xl pb-2 border-b border-slate-400">Experience</h2>

      <div class="pt-6 my-6">
        <p class="text-xl">Containerworld Forwarding Services</p>
        <p class="">Senior Software Developer <span>&#8226;</span> Dec 2020 to Present</p>
      </div>
      
      <div class="my-6">
        <p class="text-xl">Self Employed</p>
        <p class="">Full Stack Developer <span>&#8226;</span> Jan 2018 to Nov 2020</p>
      </div>
      
      <div class="my-6">
        <p class="text-xl">Siteline Systems</p>
        <p class="">Co-founder and CTO <span>&#8226;</span> Apr 2012 to Dec 2017 </p>
      </div>
      
      <div class="my-6">
        <p class="text-xl">Nimble Financial</p>
        <p class="">Co-founder <span>&#8226;</span> Mar 2011 to Mar 2012 </p>
      </div>
      
      <div class="my-6">
        <p class="text-xl">The Globe and Mail</p>
        <p class="">Director, GlobeInvestor Solutions <span>&#8226;</span> Jul 2008 to Jan 2011 </p>
      </div>
  
  
  </section>

  <section class="w-2/3 pb-48">

    <h2 class="text-3xl pb-2 border-b">Projects</h2>

    <div class="grid grid-cols-3 gap-4 mt-10">

      <ProjectCard title="Siteline Portfolio" description="Logistics Management Software for the Beverage Alcohol Industry" techSkills={['Ruby on Rails', 'PostgreSQL', 'JavaScript(ES6+)']} url="homescreen-hero.png"/>
      
      
      <ProjectCard title="React Data Table" description="Demo app using react to create a sortable, filterable, paginated data table" techSkills={['React', 'TailwindCSS', 'Parcel']} />
      
      <ProjectCard title="Interactive Dashboard Prototype" description="Proof of concept for an interactive dashboard. A full featured version of the dashboard based on this protype was rolled out to production in Siteline Portfolio." techSkills={['Chart.js', 'Grid.js', 'TailwindCSS', 'Parcel']} url="dashboard-prototype.png" />
      
      <ProjectCard title="Rails Data Table" description="Demo app using Ruby on Rails to create a sortable, filterable, paginated data table" techSkills={['Ruby on Rails', 'Stimulus.js', 'TailwindCSS', 'View Components']} />
      
      <ProjectCard title="Svelte Data Table" description="My go to application for testing new frameworks. This time using Svelte." techSkills={['Svelte', 'Svelte Kit', 'TailwindCSS']} />
      
      <ProjectCard title="Containerworld Group of Companies Website" description="Simple Landing Page for the Containerworld GOC. The client requested a book-like feel for the page with an interactive grid effect" techSkills={['JavaScript (es6+)', 'Gulp', 'Babel', 'Service Workers']}/>
    </div>


  </section>
  
  <section class="w-2/3 pb-48">

    <h2 class="text-3xl pb-2 border-b">Education</h2>

    <div class="my-6">
      <p class="text-xl">Machine Learning Certificate</p>
      <p class="">Open AI / Stanford University (Coursera)</p>
    </div>
    
    <div class="my-6">
      <p class="text-xl">Chartered Financial Analyst</p>
      <p class="">CFA Institute</p>
    </div>
    
    <div class="my-6">
      <p class="text-xl">Master of Business Administration</p>
      <p class="">Ivey Business School, Western University</p>
    </div>


  </section>

   
</div>  
