<template>
  <ejs-treegrid :dataSource="data"
    childMapping="subtasks"
    :treeColumnIndex="1"
    :allowPaging="true"
    :allowSorting="true"
    :allowFiltering="true">
    <e-columns>
      <e-column field="taskID" headerText="Task ID" width="70" textAlign="Right"></e-column>
      <e-column field='taskName' headerText='Task Name' width='200'></e-column>
      <e-column field='startDate' headerText='Start Date' width='90' format="yMd" textAlign='Right'></e-column>
      <e-column field='endDate' headerText='End Date' width='90' format="yMd" textAlign='Right'></e-column>
      <e-column field='duration' headerText='Duration' width='80' textAlign='Right'></e-column>
      <e-column field='progress' headerText='Progress' width='80' textAlign='Right'></e-column>
      <e-column field='priority' headerText='Priority' width='90'></e-column>
    </e-columns>
    </ejs-treegrid>
</template>

<script>
import {TreeGridComponent, ColumnsDirective, ColumnDirective, Page, Sort, Filter} from '@syncfusion/ej2-vue-treegrid';
import {sampleData} from './data.js';
export default {
  name: 'App',
  components: {
    'ejs-treegrid': TreeGridComponent,
    'e-columns': ColumnsDirective,
    'e-column': ColumnDirective
  },
  data:()=>{
    return{
      data: sampleData
    }
  },
  provide:{
    treegrid: [Page, Sort, Filter]
  }
}
</script>

<style>
  @import "../node_modules/@syncfusion/ej2-base/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-buttons/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-calendars/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-dropdowns/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-inputs/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-navigations/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-popups/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-splitbuttons/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-vue-grids/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-vue-treegrid/styles/material.css";
</style>
