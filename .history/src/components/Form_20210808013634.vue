<template>
    <div>
        <h2>イベントのフォーム</h2>
        <label for="title">タイトル</label>
        <input id="title" type="text" v-model="eventData.title">
        <p>{{eventData.title}}</p>
        <input id="title" type="number" v-model.number="eventData.title">
        <p>{{eventData.maxNumber}}</p>
    </div>
</template>

<script>
export default {
        data() {
            return{
            eventData:{
                title: "タイトル",
                maxNumber: 0
            },
        }
    }
}
</script>