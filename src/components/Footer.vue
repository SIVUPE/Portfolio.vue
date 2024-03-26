<template>
    <div class="container-fluid mt-5 ">
        <div class="row">
            <p class="lead text-white">
                Sivuyisiwe's porfolio &copy;
                <span>{{ currYear }}</span>
            </p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterComp',
        data() {
            return {
                currYear: new Date().getFullYear()
            }
        }
        
    }
</script>

<style scoped>
body{
    margin: 210px;
}

</style>