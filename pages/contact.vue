<template>
  	<div class="wrapper">
		<section class="hero is-fullheight">
			<div class="hero-head">
				<Navbar />
			</div>
			<div class="hero-body">
                <div class="hero-img">
                    <img src="https://d2vw2j0fzp6c9l.cloudfront.net/images/sample_photos/sample-275_XL.jpg">
                </div>
            </div>
		</section>

        <section class="container">
            <div class="columns">
                <div class="column">
                </div>
                <div class="column is-half has-text-centered">
                    <h2>KEZDŐDJÖN EL A KALAND</h2>
                    <p>Amennyiben szeretnétek, hogy pillanataitokat Mi örökítsük meg, kérj be árajánlatot.</p>
                </div>
                <div class="column">
                </div>
			    
            </div>
		</section>

		<section class="container">
            <div class="columns">
                <div class="column">
                </div>
                <div class="column is-half">
                    <ContactForm />
                </div>
                <div class="column">
                </div>
			    
            </div>
		</section>
 	</div>
</template>

<script>
import Navbar from "~/components/Navbar"
import ContactForm from "~/components/ContactForm"
export default {
    components: {
        Navbar,
        ContactForm
    }
}
</script>

<style lang="scss" scoped>
.hero.is-fullheight {
    min-height: 80vh !important;
}
</style>