<template>
    <div class="person">
        <div class="circle">
            <div class="circle-number">{{ id }}</div>
            <div class="small-circle"></div>
        </div>
        <div class="rectangle">
            <div class="name">
                <div class="name-label">Name</div>
                <div class="name-value">{{ name }}</div>
            </div>
            <div class="email">
                <div class="email-label">Email</div>
                <div class="email-value">{{ email }}</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Person',
    props: {
        id: Number,
        name: String,
        email: String
    }
}
</script>

<style scoped>
    @import '../assets/styles/person-styles.css';
</style>