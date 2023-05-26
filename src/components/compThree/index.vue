<template>
    <a-layout>
        <a-header>Header</a-header>
        <a-content>
            <div class="container">
                <div class="row">
                    <div class="col-6">
                        <a-button>Button</a-button>
                    </div>
                    <div class="col-6">
                        <a-button>
                            <a-icon type="search" />
                            Search
                        </a-button>
                    </div>
                </div>
                <div class="row">
                    <div class="col-6">
                        <a-input placeholder="Basic usage" />
                    </div>
                    <div class="col-6">
                        <a-input prefix="Prefix" />
                    </div>
                </div>
                <div class="row">
                    <div class="col-6">
                        <a-select style="width: 100%;">
                            <a-select-option value="jack">Jack</a-select-option>
                            <a-select-option value="lucy">Lucy</a-select-option>
                            <a-select-option value="disabled" disabled>
                                Disabled
                            </a-select-option>
                            <a-select-option value="Yiminghe">yiminghe</a-select-option>
                        </a-select>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <a-table :columns="columns" :data-source="data"></a-table>
                    </div>
                </div>
            </div>
        </a-content>
        <a-footer>Footer</a-footer>
    </a-layout>
</template>
  
<script>
import { defineComponent } from 'vue';
import { Layout, Button, Input, Select, Table, Icon } from 'ant-design-vue';

export default defineComponent({
    name: 'ComPage',
    components: {
        'a-layout': Layout,
        'a-header': Layout.Header,
        'a-content': Layout.Content,
        'a-footer': Layout.Footer,
        'a-button': Button,
        'a-input': Input,
        'a-select': Select,
        'a-select-option': Select.Option,
        'a-table': Table,
        'a-icon': Icon,
    },
    data() {
        return {
            columns: [
                {
                    title: 'Name',
                    dataIndex: 'name',
                },
                {
                    title: 'Age',
                    dataIndex: 'age',
                },
                {
                    title: 'Address',
                    dataIndex: 'address',
                },
            ],
            data: [
                {
                    key: '1',
                    name: 'John Brown',
                    age: 32,
                    address: 'New York No. 1 Lake Park',
                },
                {
                    key: '2',
                    name: 'Jim Green',
                    age: 42,
                    address: 'London No. 1 Lake Park',
                },
                {
                    key: '3',
                    name: 'Joe Black',
                    age: 32,
                    address: 'Sidney No. 1 Lake Park',
                },
            ],
        };
    },
});
</script>
  
<style scoped>
.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
}

.row {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;
}

.col-6 {
    flex-basis: 50%;
    padding: 0 10px;
}

.col-12 {
    flex-basis: 100%;
    padding: 0 10px;
}
</style>