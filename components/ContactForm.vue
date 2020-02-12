<template>
    <div class="contact-form-wrapper">
        <form action="/submission" name="contact" method="POST" data-netlify="true">
            <div class="field">
                <label class="label">NÉV *</label>
                <div class="control">
                    <input class="input" type="text" name="Name">
                </div>
            </div>

            <div class="field">
                <label class="label">E-MAIL CÍM *</label>
                <div class="control">
                    <input class="input" type="text" name="Email">
                </div>
            </div>

            <div class="field">
                <label class="label">MILYEN TÍPUSÚ FOTÓZÁS ÉRDEKELNE? *</label>
                <div class="control">
                    <label class="radio">
                    <input type="radio" name="Jegyes">
                    Jegyes
                    </label>
                    <br>
                    <label class="radio">
                    <input type="radio" name="Esküvői">
                    Esküvői
                    </label>
                    <br>
                    <label class="radio">
                    <input type="radio" name="Család">
                    Család
                    </label>
                </div>
            </div>

            <div class="field">
                <label class="label">HONNAN HALLOTTÁL RÓLUNK?</label>
                <div class="control">
                    <div class="select is-primary">
                        <select name="Source">
                            <option></option>
                            <option>Facebook</option>
                            <option>Instagram</option>
                            <option>Google</option>
                            <option>Ismerős</option>
                            <option>Egyéb</option>
                        </select>
                    </div>
                </div>
            </div>
            
            <div class="field">
                <label class="label">ÜZENETED SZÁMUNKRA *</label>
                <div class="control">
                    <textarea class="textarea" name="Message"></textarea>
                </div>
            </div>

            
            <div class="control has-text-centered">
                <button class="button is-primary" type="submit">Küldés</button>
            </div> 
        </form>
    </div>
</template>

<script>
export default {
}
</script>

<style lang="scss">
.contact-form-wrapper {
    background-color: #fff;
    padding: 60px;
}
</style>