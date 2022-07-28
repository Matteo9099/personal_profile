<template>

    <div class="card pb-5" style="width: 18rem;">
       <img :src="require(`../assets/img/${image}`)" :alt="title">
        <div class="card-body ms_overflow_card">
            <h5 class="card-title">{{ title }}</h5>
            <p class="card-text">{{ content }}</p>
        </div>
    </div>

</template>

<script>
export default {
    name: 'CardComponent',
    props: ['slides', 'image', 'title', 'content', 'badge'],
}
</script>

<style scoped lang="scss">
img {
    height: 200px;
    object-fit: cover;
}
</style>


