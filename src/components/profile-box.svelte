<script lang="ts">
    import ThemeToggle from './theme-toggle.svelte';
	import { FontAwesomeIcon } from 'fontawesome-svelte';
	import { faGithub, faLinkedin } from '@fortawesome/free-brands-svg-icons';
	import { faEnvelope } from '@fortawesome/free-solid-svg-icons';
</script>

<div class="profile-box">

	<div class="pic"></div>
	<h1>Jigar Patel</h1>

    <hr />

	<div class="socials">
		<!-- <a
			class="social-icon github"
			target="_blank"
			href="https://github.com/jigu210">
			<FontAwesomeIcon icon={faGithub}></FontAwesomeIcon>
		</a> -->
		<a
			class="social-icon email"
			href="mailto:jigarkpat@gmail.com">
			<FontAwesomeIcon icon={faEnvelope}></FontAwesomeIcon>
		</a>
	</div>

	<hr />

    <ThemeToggle></ThemeToggle>

</div>

<style lang="scss">
	@use "sass:math";
	.profile-box
	{
		text-align: center;
		max-width: 360px;
		margin: 0 auto;

		// > .pic
		// {
		// 	$pic-size: 120px;

		// 	display: inline-block;
		// 	width: $pic-size;
		// 	height: $pic-size;
		// 	border-radius: math.div($pic-size, 2);
		// 	background-size: cover;
		// 	background-position: center center;
		// 	background-repeat: no-repeat;
		// 	background-color: black;
		// }

		h1
		{
			color: var(--primary-font-color);
			font-family: 'Roboto Mono';
			max-width: 240px;
			margin: 10px auto;
		}

        hr
        {
            border: 1px solid var(--primary-font-color);
            opacity: 0.2;
            margin: 24px auto;
            max-width: 200px;
        }

		> .socials
		{
			a
			{
				color: var(--primary-font-color);
				font-size: 150%;
				vertical-align: middle;

				&:not(:last-child)
				{
					margin-right: 10px;
				}
			}
		}
	}
</style>
