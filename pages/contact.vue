<template>
    <div class="container">
        <Navbar />
        <div class="columns">
            <div class="column">
            </div>
            <div class="column is-one-third">
                <form action="/submission" name="contact" method="POST" data-netlify="true">  
                    <input class="input" type="text" name="name" placeholder="Név (kötelező)">
                    <input class="input" type="text" name="email" placeholder="E-mail cím (kötelező)">
                    <input class="input" type="tel" name="telephone" placeholder="Telefonszám">
                    <textarea class="textarea" name="message" placeholder="Kérlek írj magadról és az elképzeléseidről pár sort."></textarea>
                    <div class="control">
                        <button class="button is-primary" type="submit">Küldés</button>
                    </div> 
                </form>
            </div>
            <div class="column">
            </div>
        </div>
    </div>
</template>

<script>
import Navbar from "~/components/Navbar"
export default {
    components: {
        Navbar
    }
}
</script>