<script setup>
    const props = defineProps(['cadastrarTarefa','tarefaTemp','trocarFiltro', 'editaTarefaTemp'])
</script>

<template>
    <form @submit.prevent="props.cadastrarTarefa">
        <div class="row">
            <div class="col-md-4">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required 
                type="text" placeholder="Digite aqui a descriçao da tarefa" class="form-control">
            </div>
            <div class="col">
                <button type="" class="btn btn-primary">Cadastrar</button>
            </div>
            <div class="col">
                <select @change="props.trocarFiltro" class="form-control">
                    <option value="todas">todas Tarefas</option>
                    <option value="pendentes">Pendentes</option>
                    <option value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>