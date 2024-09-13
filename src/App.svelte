<script lang="ts">

	import ProfileBox from './components/profile-box.svelte';
	import { WorkProjects } from './data/work_projects';
	import ProjectsList from './components/projects-list.svelte';
	import { Repos } from './data/open_source_repos';
	import ReposList from './components/repos-list.svelte';

	const started_coding_age = 9;
	const started_coding_year = 1996 + started_coding_age;
	const building_software_years = (new Date()).getFullYear() - started_coding_year;

</script>

<div class="app">
	<div class="left">
		<ProfileBox />
	</div>
	<div class="right">
		<!-- <div class="section">
			<h3>About</h3>
		</div> -->
		<div class="section">
			<h3>Work &amp; Experience</h3>
			<ProjectsList projects={WorkProjects}></ProjectsList>
		</div>
		<div class="section">
			<!-- <h3>Open Source</h3>
			<ReposList repos={Repos}></ReposList> -->
		</div>
		<div class="copyright">
			&copy; { new Date().getFullYear() } Jigar Patel
		</div>
	</div>
</div>

<style lang="scss">
	.app
	{
		max-width: 1000px;
		padding: 20px;
		margin: 0 auto;

		// > .left
		// {	
		// }

		> .right
		{
			> .section
			{
				margin-bottom: 32px;

				h3
				{
					font-family: 'Roboto Mono';
				}

				p
				{
					color: rgba(var(--primary-font-color-rgb), 0.7);
					line-height: 140%;
					font-size: 95%;
				}
			}

			> .copyright
			{
				border-top: 2px solid rgba(var(--primary-font-color-rgb), 0.2);
				padding: 20px 0;
				text-align: center;
				font-size: 80%;
				color: rgba(var(--primary-font-color-rgb), 0.7);
			}
		}

		@media screen and (min-width: 800px) {
			display: flex;

			> .left
			{
				flex-grow: 0;
				flex-shrink: 0;
				width: 260px;
			}

			> .right
			{
				flex-grow: 1;
				flex-shrink: 1;
				padding-left: 20px;
				min-width: 0;
			}
		}
	}
</style>
