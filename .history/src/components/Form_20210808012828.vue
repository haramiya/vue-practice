<template>
    <div>
        <h2>イベントのフォーム</h2>
        <label for="title">タイトル</label>
        <input id="title" type="text" v-model="eventData.title">
        <p>{{eventData.title}}</p>
    </div>
</template>

<script>
export default {
    data() {
        return{
        eventData:{
            title: "タイトル"
        }
    }
}
</script>