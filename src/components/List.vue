<script setup>
    import useTodos from "../composables/useTodos";
    
    const { pending, completed, changeStatus } = useTodos();

    defineProps({
        isCompleted: {
            default: false,
            type: Boolean,
        },     
    });

</script>
<template>
    <div class="w-1/3">
        <h3 class="text-2xl text-center" :class ="isCompleted ? 'text-blue-400': 'text-purple-400'">
            {{isCompleted ? "Completed" : "Pending"}}
        </h3>
        <ul class="pt-8 space-y-4">
            <li
                @click="changeStatus(todo.id)" 
                v-for="todo in isCompleted ? completed : pending"
                :key="todo.id"
                :class="isCompleted 
                    ? 'text-yellow-600 hover:bg-yellow-400' 
                    : 'text-orange-600 hover:bg-orange-400'"
                class="w-full px-4 py-2 font-bold text-center duration-500 bg-gray-300 rounded-lg hover:cursor-pointer hover:text-gray-200">
                  {{ todo.content }}
            </li>
        </ul>
    </div>
</template>