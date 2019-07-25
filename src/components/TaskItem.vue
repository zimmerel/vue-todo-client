<template>
    <li>
        <h4 class="title">{{title}}</h4>
        <div class="content">
            <ul>
                <li><font-awesome-icon icon="plus-circle" size="3x"></font-awesome-icon></li>
            </ul>
        </div>
    </li>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class TaskItem extends Vue {
    @Prop() private title!: string;

    add() {
        // Logic to flip this component to an actual task
        // emit event so list will add new item
    }
}
</script>
