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
            
            <div class="columns">
                <div class="column has-text-centered">
                    <h1>{{pageTitle}}</h1>
                </div>
            </div>
        </section>

        <section class="container">
            <Grid />
        </section>
    </div>          
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
        path: this.$route.params.name
        }
    },
    computed: {
        pageTitle () {
            if(this.path === 'eljegyzes') {
                return 'Eljegyzés'
            }
            if (this.path === 'eskuvo') {
                return 'Esküvő'
            }
            if(this.path === 'csalad') {
                return 'Család'
            }
        }
    }
}
</script>


<style lang="scss">
</style>
