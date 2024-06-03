<template>
    <div>
        <h2>콘솔을 확인합니다.</h2>
    </div>
</template>

<script setup>
import axios from 'axios';

// todos에서 id가 1인 목록 출력
// const requestAPI = () => {
//     // const url = 'http://localhost:3000/todos/1';
//     const url = '/api/todos/1';
//     axios.get(url).then((response) => {
//         console.log('# 응답객체 : ', response);
//     });
// };

//todos에서 목록 콘솔 출력 후 id가 1인 목록 콘솔 출력
// const listUrl = '/api/todos';
// const todoUrlPrefix = '/api/todos/';

// const requestAPI = () => {
//     let todoList = [];
//     axios
//         .get(listUrl)
//         .then((response) => {
//             todoList = response.data;
//             console.log('# TodoList : ', todoList);
//             return todoList;
//         })
//         .then((todoList) => {
//             todoList.forEach((e) => {
//                 if (e.id === '1') {
//                     console.log(e);
//                 }
//             });
//         });
// };

const listUrl = '/api/todos';
const todoUrlPrefix = '/api/todos/';
const requestAPI = async () => {
    let todoList;

    let response = await axios.get(listUrl);
    todoList = response.data;
    console.log('# TodoList : ', todoList);
};

requestAPI();
</script>
