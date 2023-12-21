<script>
import Bar from '../Bar.vue';
import MainButton from '../MainButton.vue';

export default {
    name: 'Form',
    props: ['titolo', 'sottotitolo'],
    components: { Bar, MainButton },
    data() {
        return {
            buttonContent: 'Send'
        }
    }
}
</script>

<template>
    <h2>{{ titolo }}<span class="dot">.</span></h2>
    <p>{{ sottotitolo }}</p>
    <Bar />
    <div class="form">
        <form action="">
            <!-- input per nome e email  -->
            <div class="input-text">
                <input type="text" placeholder="Your Name">
                <input type="text" placeholder="Your Email">
            </div>
            <!-- area di testo  -->
            <div class="text-area">
                <textarea placeholder="Write a message..." rows="6"></textarea>
            </div>
            <!-- submit  -->
            <MainButton :testoBottone="buttonContent" class="form-button" />
        </form>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/partials/variables' as *;

h2 {
    font-size: 42px;
}

p {
    margin-top: 15px;
    margin-bottom: 30px;
}

.input-text {
    display: flex;
    gap: 25px;
    margin-top: 50px;

    input {
        width: 50%;
        outline: 0;
        border-width: 0 0 2px;
        padding: 0 0 10px 20px;
    }
}

textarea {
    width: 100%;
    outline: 0;
    border-width: 0 0 2px;
    margin-top: 25px;
    padding-left: 25px;
}

.form-button {
    color: $white;
    background-color: $secondary-color;
    margin-top: 40px;
}
</style>