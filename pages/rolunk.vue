<template>
  	<div class="wrapper">
		<section class="hero is-fullheight">
			<div class="hero-head">
				<Navbar />
			</div>
			<div class="hero-body">
                <div class="hero-img image is-3by1">
                    <img src="https://d2vw2j0fzp6c9l.cloudfront.net/images/sample_photos/sample-275_XL.jpg">
                </div>
            </div>
		</section>

        <section class="container">
            <div class="columns">
                <div class="column">
                </div>
                <div class="column is-three-quarters has-text-centered">
                    <h2>AZ NR PHOTO TÖRTÉNETE</h2>
                </div>
                <div class="column">
                </div>
            </div>
		</section>

        <section class="container">
            <div class="columns">
                <div class="column">
                </div>
                <div class="column is-three-quarters">
                    <p>Egy pár életében több olyan fontos esemény van, melyet meg kell örökíteni.
                        Ilyenek közé tartozik az eljegyzés, az esküvő, a babavárás vagy a gyermekek fotózása.
                        Fontos pillanatok, emlékek, melyeket képekben örökítünk meg.
                        Hisszük, hogy a pillanat szépsége és a fotós szenvedélye együtt eredményezi "A fotót".</p>
                </div>
                <div class="column">
                </div>
            </div>
		</section>

        <section class="container">
            <div class="columns">
                <div class="column">
                </div>
                <div class="column is-three-quarters">
                    <p>Azt "A fotót", amit örömmel mutattok meg barátaitoknak, családtagjaitoknak, amit a falra, polcra, albumba, közösségi oldalakra téve bármikor rápillantva öröm fog el benneteket.
                        Ezekért a képekért felelünk Mi: Eszti és Ricsi.
                        Szenvedéllyel, szeretettel és szívből tesszük mindezt ketten, hogy minden fontos pillanatot meg tudjunk örökíteni, különleges hangulatot teremtve,
                        a női és férfi meglátással kiegészülve.</p>
                </div>
                <div class="column">
                </div>
            </div>
		</section>

        <section class="container">
            <div class="columns">
                <div class="column">
                </div>
                <div class="column is-three-quarters">
                    <figure class="image is-4by3">
                        <img src="https://bulma.io/images/placeholders/480x480.png">
                    </figure>
                </div>
                <div class="column">
                </div>
            </div>
		</section>

        <section class="container">
			<div class="columns">
				<div class="column">
				</div>
				<div class="column has-text-centered">
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
import ContactForm from "~/components/ContactForm"
import Parallax from "vue-parallaxy";

export default {
    components: {
        Navbar,
        ContactForm,
        Parallax
    }
}
</script>

<style lang="scss" scoped>
.hero.is-fullheight {
    min-height: 80vh !important;
}
</style>