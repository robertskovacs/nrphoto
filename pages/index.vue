<template>
  	<div class="wrapper">
		<section class="hero is-fullheight">
			<div class="hero-head">
				<Navbar />
			</div>
			<div class="hero-body">
				<Carousel/>
			</div>
		</section>

		<section class="container">
			<div class="columns">
				<div class="column">
					<h1>HI, I AM STANLEY</h1>
					<h3>YOUR STORY STARTS HERE</h3>
				</div>

				<div class="column">
					<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.
						Praesent nec felis libero. Ut blandit viverra urna quis scelerisque.
						Praesent non venenatis ex. Morbi in pellentesque dui. Aliquam erat volutpat.
						Nam imperdiet, eros quis mattis mollis, elit ligula egestas nisi, scelerisque cursus enim orci in nisl.
						Phasellus eros metus, rutrum quis dapibus a, interdum et elit.</p>
					<p>Morbi non velit at nibh vulputate tincidunt. Nulla varius pellentesque dolor, quis accumsan mi aliquam ac.
						Aenean bibendum, libero eget feugiat condimentum, elit arcu fermentum nibh, in mattis sapien leo in felis.
						Etiam scelerisque turpis luctus, rutrum ex placerat, malesuada ipsum. Sed non ex vitae erat dictum pharetra.
					</p>
				</div>
			</div>

			

			
		</section>

		<section class="container">
			<div class="columns">
				<div class="column">
					<img class="image is-300x300" src="https://bulma.io/images/placeholders/480x480.png">
				</div>

				<div class="column">
					<h1>Filozófiánk</h1>
					<h3>YOUR STORY STARTS HERE</h3>
					<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.
						Praesent nec felis libero. Ut blandit viverra urna quis scelerisque.
						Praesent non venenatis ex. Morbi in pellentesque dui. Aliquam erat volutpat.
						Nam imperdiet, eros quis mattis mollis, elit ligula egestas nisi, scelerisque cursus enim orci in nisl.
						Phasellus eros metus, rutrum quis dapibus a, interdum et elit.</p>
					
				</div>
			</div>
		</section>

		<section class="container" id="pillanatok">
			<div class="columns">
				<div class="column has-text-centered">
					<h1>ÁLTALUNK MEGÖRÖKÍTETT PILLANATOK</h1>
				</div>
			</div>
			<div class="columns">
				<div class="column">
					<nuxt-link to="/pillanatok/eljegyzes">
						<img class="image is-300x300" src="https://bulma.io/images/placeholders/480x480.png">
						<div class="has-text-centered">
							<h2>Eljegyzés</h2>
							<h3>Valami új kezdete</h3>
						</div>
					</nuxt-link>
				</div>
				<div class="column">
					<nuxt-link to="/pillanatok/eskuvo">
						<img class="image is-300x300" src="https://bulma.io/images/placeholders/480x480.png">
						<div class="has-text-centered">
							<h2>Esküvő</h2>
							<h3>A nagy nap</h3>
						</div>
					</nuxt-link>
				</div>
				<div class="column">
					<nuxt-link to="/pillanatok/csalad">
						<img class="image is-300x300" src="https://bulma.io/images/placeholders/480x480.png">
						<div class="has-text-centered">
							<h2>Család</h2>
							<h3>Babavárás, gyerekkor</h3>
						</div>
					</nuxt-link>
				</div>
			</div>
		</section>

		<section class="container">
			<div class="columns">
				<div class="column">
				</div>
				<div class="column">
					<a href="/contact">
						<button class="button is-primary">Lépj velünk kapcsolatba</button>
					</a>
				</div>
				<div class="column">
				</div>
			</div>
		</section>





 	</div>
</template>

<script>
import Navbar from "~/components/Navbar"
import Carousel from "~/components/Carousel"
export default {
    components: {
		Navbar,
		Carousel
	},
}
</script>

<style>


.carousel {
	position: relative;
    overflow: hidden;
}
.carousel, img {
	position: absolute;
    object-fit: cover; /*magic*/
    object-position: center center;
    width: 100%;
	height: 100%;
}

.hero-body {
	padding:0 !important;
}

.hero-head {
	position: absolute;
	width: 100%;
}

.carousel-nav-next {
	position: relative;
    z-index: 1;
	color: white;
	float: right;
	top:50%;
	margin-right:3rem;
	font-size: 50px;
}

.carousel-nav-prev {
	position: relative;
    z-index: 1;
	color: white;
	float: left;
	top:50%;
	margin-left:3rem;
	font-size: 50px;
}

.nain-logo-wrapper {
	position:relative;
}

.main-logo, .main-logo.img {
	height:auto !important;
	width: 120px !important;
	min-height:0 !important;
	display: block !important;
	position:absolute;
	bottom:0;
	left:43%;
}

</style>
