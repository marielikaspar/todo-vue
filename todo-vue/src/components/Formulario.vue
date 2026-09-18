<script setup>
const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>



<template>
      <form @submit.prevent="props.cadastraTarefa" >
            <div class="row">
                <div class="col">
                    <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required type="text" class="form-control" placeholder="Adicione uma nova tarefa">
                </div>
                <div class="col-auto">
                    <button type="submit" class="btn btn-primary">Adicionar</button>
                </div>
                <div class="col-md-2">
                    <button type="submit" class="btn btn-primary">Cadastrar</button>
                </div>
                <div class="col-md-2">
                    <select @change="props.trocarFiltro" class="form-control">
                        <option value="todas">Todas as tarefas</option>
                        <option value="pending">Pendentes</option>
                        <option value="completed">Concluídas</option>
                    </select>
                </div>
            </div>
            
        </form>
</template>