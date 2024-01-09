<script>
export default {
    name: 'AppMain',
    data() {
        return {
            
        }
    },
}
</script>

<template>
    <main>
        <div class="container d-flex py-5">
            <h3>&ndash;&ndash;&gt;Content goes here!&lt;&ndash;&ndash;</h3>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/_variables.scss' as *;
    
    main{
        background-color: #1c1c1c;

        h3{
            color: #fff;
        }
    }
</style>