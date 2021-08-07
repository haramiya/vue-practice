<template>
    <div>
        <h2>イベントのフォーム</h2>
        <label for="title">タイトル：</label>
        <input id="title" type="text" v-model="eventData.title">
        <p>タイトルの内容：{{eventData.title}}</p>
        <label for="maxNumber">最大人数：</label>
        <input id="maxNumber" type="number" v-model.number="eventData.maxNumber">
        <p>最大人数の内容：{{eventData.maxNumber}}</p>
        <label for="host">主催者：</label>
        <input id="host" type="text" v-model.trim="eventData.host">
        <p>主催者の内容：{{eventData.host}}</p>
        <label for="textarea">テキストエリア：</label>
        <textarea id="detail" cols="30" rows="10" v-model="eventData.detail"></textarea>
        <pre>テキストエリアの内容：{{eventData.detail}}</pre>
        <label for="isPrivate">非公開</label>
        <input type="checkbox" id="isPrivate" v-model="eventData.isPrivate">
        <p>{{eventData.isPrivate}}</p>
        <p>参加条件</p>
        <label for="10">10代</label>
        <input type="checkbox" id="10" value="10代" v-model="eventData.target">
        <label for="20">20代</label>
        <input type="checkbox" id="20" value="20代" v-model="eventData.target">
        <label for="30">30代</label>
        <input type="checkbox" id="30" value="30代" v-model="eventData.target">
        <label for="40">40代</label>
        <input type="checkbox" id="40" value="40代" v-model="eventData.target">
        <p>参加条件の内容：{{eventData.target}}</p>
        <p>参加費</p>
        <label for="free">無料</label>
        <input type="radio" id="free" value="無料" v-model="eventData.price">
        <label for="paid">有料</label>
        <input type="radio" id="paid" value="有料" v-model="eventData.price">
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
                detail: "",
                isPrivate: false,
                target: [],
                price: "無料"
            },
        }
    }
}
</script>