<template lang="">
<v-app-bar app color="black" flat class="px-12">
    <v-btn>
        <v-icon color="blue-darken-4" left class="mr-2">
            fas fa-signature
        </v-icon>
        TPhat
    </v-btn>
        <v-spacer></v-spacer>
        <v-btn text @click="scroll('home')" class="text-blue-darken-4">Home</v-btn>
        <v-btn text @click="scroll('about')" >About</v-btn>
        <v-btn text @click="scroll('portfolio')" >Portfolio</v-btn>
        <v-btn text @click="scroll('services')" >Services</v-btn>
        <v-btn text @click="scroll('page')" >Page</v-btn>
        <v-btn text @click="scroll('blog')" >Blog</v-btn>
        <v-btn text @click="scroll('contact')" >Contact</v-btn>

</v-app-bar>
</template>

<script>
export default {
    methods: {
        scroll(refName) {
            const element = document.getElementById(refName)
            element.scrollIntoView({ behavior: "smooth" })
        }
    }
};
</script>

<style lang=""></style>
