<template>
    <div class="wrapper">
		<section class="hero">
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
            <Grid />
        </section>
    </div>
    <!--
    <div class="tile is-ancestor">
        <div class="tile is-vertical">
            <div class="tile">

            <div class="tile is-parent is-vertical">
                <article class="tile is-child">
                <figure class="image is-3by5">
                    <img src="https://bulma.io/images/placeholders/640x480.png">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://bulma.io/images/placeholders/640x480.png">
                </figure>
                </article>
            </div>
            
            <div class="tile is-parent is-vertical">
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://bulma.io/images/placeholders/640x480.png">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by5">
                    <img src="https://bulma.io/images/placeholders/640x480.png">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://bulma.io/images/placeholders/640x480.png">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://bulma.io/images/placeholders/640x480.png">
                </figure>
                </article>
            </div>

            <div class="tile is-parent is-vertical">
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://bulma.io/images/placeholders/640x480.png">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by5">
                    <img src="https://bulma.io/images/placeholders/640x480.png">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://bulma.io/images/placeholders/640x480.png">
                </figure>
                </article>
            </div>

            </div>
        </div>
    </div>
    -->
</template>

<script>
import Navbar from "~/components/Navbar"
import Grid from "~/components/Grid"
export default {
    components: {
        Navbar,
        Grid
    },
    data() {
    return {
      name: this.$route.params.name
    }
  }
}
</script>


<style lang="scss">
</style>
