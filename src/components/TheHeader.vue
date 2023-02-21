<script>
import { store } from '../store';
export default {
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container ">
            <a>Boolfolio</a>
            <div class="">
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup"
                    aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
                    <div class="navbar-nav">
                        <a class="nav-item nav-link active" href="#">Home <span class="sr-only">(current)</span></a>
                        <a class="nav-item nav-link" href="#">Project</a>
                        <a class="nav-item nav-link" href="#">Chi siamo</a>
                        <a class="nav-item nav-link" href="#">Contatti</a>
                    </div>
                </div>
            </div>

        </div>
    </nav>
</template>

<style lang="scss">
@use "../styles/main";
@use "bootstrap/scss/bootstrap";
</style>