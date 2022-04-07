<template>
    <div class = "page">
        <h3>{{$route.params.page}}페이지입니다</h3>
        <li v-for = "item in boards" :key = "item.id">
            <div :id = "item.id">
                <p>{{item.memo}}</p>
            </div>
        </li>
    </div>
</template>

<script>
// @ is an alias to /src
//json 파일
import board from "@/assets/data/data.json";

export default {
    name: 'PageComponent',
    data: () => ({
        boards: board
    })
}
</script>