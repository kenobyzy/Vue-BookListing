<template>
    <form class="" action="#" @submit.prevent="bookSubmit(bookTitle, bookAuthor)">
        <input v-model="bookTitle" type="text" name="title" value="" placeholder="Book Title">
        <input v-model="bookAuthor" type="text" name="author" value="" placeholder="Book Author">
        <button type="submit" name="button">Add Book</button>
    </form>
</template>

<script>
export default {
    name: "BookForm",
    props: [
        "books"
    ],
    data: () => ({
        bookTitle: "",
        bookAuthor: ""
    }),
    methods: {
        bookSubmit(bookTitle, bookAuthor) {
            this.$emit("addBook", bookTitle, bookAuthor)
        }
    }

}
</script>

<style>

</style>