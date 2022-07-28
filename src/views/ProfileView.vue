<template>

    <div class="d-flex justify-content-center align-items-center flex-column vh-100 bg-dark position-relative">
        <div class="bg_photo"></div>
        <div class="profession my-3 animate__animated animate__fadeIn">
            <h2 class="text-white">Full Stack Web Developer</h2>
        </div>
        <p class="text-white">
            <button class="btn btn-warning ms_button_relative mb-5 animate__animated animate__fadeIn" type="button" data-bs-toggle="collapse"
                data-bs-target="#collapseWidthExample" aria-expanded="false" aria-controls="collapseWidthExample">
                CHI SONO
            </button>
        </p>
        <div style="min-height: 120px;">
            <div class="collapse collapse-horizontal animate__animated animate__fadeIn ms_button_relative" id="collapseWidthExample">
                <div class="text-white mt-5" style="width: 300px;">
                    <p>Appassionato di informatica e design, inizio i miei studi per diventare programmatore web nel 2020, frequentando e superando i corsi di <a class="nav-link text-warning" href="https://boolean.careers/" target="_blank">BOOLEAN CARRERS</a> come sviluppatore Full Stack, e dell'<a class="nav-link text-warning" href="https://www.istitutovolta.eu/" target="_blank">ISTITUTO VOLTA</a> studiando Java.</p>
                </div>
            </div>
        </div>

        <div class="lines">
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
        </div>

    </div>

</template>

<script>

export default {
    name: 'ProfileView',

}
</script>

<style scoped>

.bg_photo{
    background: url('../assets/img/matteo_img.png') no-repeat;
    position: absolute;
    height: 100%;
    width: 100%;
    opacity: 0.1;
    background-position: top;
}

</style>