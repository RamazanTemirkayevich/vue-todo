<template>
    <form @submit.prevent="onSubmit">
        <input type="text" v-model="title">
        <button type="submit">Add New</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            title: ''
        }
    },
    methods: {
        onSubmit() {
            console.log('submit', this.title);
            if (this.title.trim()) {
                const newTodo = {
                    id: Date.now(),
                    title: this.title,
                    completed: false
                }

                this.$emit('add-todo', newTodo)
                this.title = ''
            }
        }
    }
}
</script>

<style scoped>
    form {
        display: flex;
        justify-content: space-between;
    }

    input {
        margin: 0 auto;
        width: 50%;
        height: 30px;
    }

    button {
        background: blue;
        color: #fff;
        text-transform: uppercase;
        border-radius: 10%;
        border: none;
        font-size: 14px;
        margin-right: 0;
    }
</style>