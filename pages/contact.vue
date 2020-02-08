<template>
    <div class="contact">
        <div class="columns">
            <div class="column">
            </div>
            <div class="column is-one-third">
                <form name="contact" method="POST" data-netlify="true">  
                    <input class="input" type="text" placeholder="Név (kötelező)">
                    <input class="input" type="text" placeholder="E-mail cím (kötelező)">
                    <input class="input" type="tel" placeholder="Telefonszám">
                    <textarea class="textarea" placeholder="e.g. Hello world"></textarea>
                    <div class="control">
                        <button class="button is-primary" type="submit">Submit</button>
                    </div>
                    
                </form>
            </div>
            <div class="column">
            </div>
        </div>
    </div>
</template>