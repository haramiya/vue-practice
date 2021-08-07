<template>
    <div>
        <h2>イベントのフォーム</h2>
        <label for="title">タイトル：</label>
        <input id="title" type="text" v-model="eventData.title">
        <p>タイトルの内容：{{eventData.title}}</p>
        <label for="title">最大人数：</label>
        <input id="title" type="number" v-model.number="eventData.maxNumber">
        <p>最大人数の内容：{{eventData.maxNumber}}</p>
        <label for="title">主催者：</label>
        <input id="title" type="text" v-model.trim="eventData.host">
        <p>主催者の内容：{{eventData.host}}</p>
        <label for="title">テキストエリア：</label>
        <textarea id="detail" cols="30" rows="10" v-model="eventData.detail"></textarea>
        <p>テキストエリアの内容：{{eventData.detail}}</p>
    </div>
</template>

<script>
export default {
        data() {
            return{
            eventData:{
                title: "タイトル",
                maxNumber: 0,
                host: "",
                detail: ""
            },
        }
    }
}
</script>