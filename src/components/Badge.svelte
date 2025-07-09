<script lang="ts">
	import { sql } from "@evolu/react";


  type IconKey = keyof typeof iconClasses;

  let { label = "Badge", color = "white", size = "medium", icon = "" }: {
    label?: string;
    color?: string;
    size?: "small" | "medium" | "large";
    icon?: IconKey | "" | null;
  } = $props();

  const iconClasses = {
    heroku: 'devicon--heroku',
    javascript: 'devicon--javascript',
    postgresql: 'devicon--postgresql',
    rails: 'devicon--rails-wordmark',
    linkedin: 'devicon--linkedin',
    github: 'devicon--github',
    redis: 'devicon--redis',
    memcached: 'devicon--memcached',
    tailwindcss: 'devicon--tailwindcss',
    stimulus: 'devicon--stimulus',
    hotwire: 'devicon--hotwire',
    rspec: 'devicon--rspec',
    python: 'devicon--python',
    go: 'devicon--go',
    nodejs: 'devicon--nodejs',
    typescript: 'devicon--typescript',
    react: 'devicon--react',
    vuejs: 'devicon--vuejs',
    svelte: 'devicon--svelte',
    docker: 'devicon--docker',
    figma: 'devicon--figma',
    sketch: 'devicon--sketch',
    elasticsearch: 'devicon--elasticsearch',
    postman: 'devicon--postman',
    sqlite: 'devicon--sqlite',
  }

</script>

<div class="flex gap-x items-center px-3 py-2 rounded-md border dark:border-slate-600  bg-{color} dark:bg-slate-700 {size == "small" ? 'text-sm px-2 py': ''}">
  {#if icon}
    <span class="iconify-color {iconClasses[icon]} h-6 w-6 mr-1"></span>
  {/if}
  {label}
</div>