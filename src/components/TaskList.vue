<template>
    <div>
        <h1 class="title">{{title}}</h1>
        <div class="content">
            <ul>
                <li><font-awesome-icon icon="plus-circle" size="3x"></font-awesome-icon></li>
            </ul>
        </div>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import TaskItem from '@/components/TaskItem.vue';

@Component({
    components: {TaskItem}
})
export default class TaskList extends Vue {
  @Prop() private title!: string;
  @Prop() private taskItems: Array<TaskItem> = [];
}
</script>
