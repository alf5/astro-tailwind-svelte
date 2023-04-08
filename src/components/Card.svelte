<script lang="ts">
export let title: string;
export let body: string;
export let href: string;
</script>

<li class="link-card group">
	<a href={href}>
		<h2>
			{title}
			<span>&rarr;</span>
		</h2>
		<p>
			{body}
		</p>
	</a>
</li>

<style lang="css">
	.link-card {
    @apply hover:bg-[position:0] hover:bg-[image:var(--accent-gradient)]
           focus-within:bg-[position:0] focus-within:bg-[image:var(--accent-gradient)]
           bg-[image:none] bg-[size:400%] bg-[position:100%] list-none flex p-1 bg-white rounded-lg
           transition-[background-position] duration-700 ease-[cubic-bezier(0.22,1,0.36,1)] shadow-md;
	}

	.link-card > a {
    @apply w-full no-underline leading-6 py-3 px-4 rounded-md text-neutral-900 bg-white opacity-80;
	}
	h2 {
		transition: color 0.6s cubic-bezier(0.22, 1, 0.36, 1);
    @apply m-0 text-xl group-hover:text-[rgb(var(--accent))] group-focus-within:text-[rgb(var(--accent))] transition-[color] duration-700 ease-[cubic-bezier(0.22,1,0.36,1)];
	}
	p {
    @apply mt-2 mb-0 text-neutral-700;
	}
  span {
    @apply text-cyan-700 hover:text-red-500;
  }
</style>
