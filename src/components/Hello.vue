<template>
  <div class="hello">
    <kendo-buttongroup>
      <kendo-buttongroup-button> Button 1 </kendo-buttongroup-button>
      <kendo-buttongroup-button> Button 2 </kendo-buttongroup-button>
      <kendo-buttongroup-button> Button 3 </kendo-buttongroup-button>
    </kendo-buttongroup>
    <div class="grid">
      <kendo-datasource 
        ref="datasource"
        :type="'odata'"
        :pageSize="20"
        :transportRead="'https://demos.telerik.com/kendo-ui/service/Northwind.svc/Customers'"
      ></kendo-datasource>
      <kendo-grid
        :height="550"
        :dataSourceRef="'datasource'"
        :groupable='true'
        :sortable='true'
        :pagearble-refresh='true'
        :pageable-page-sizes='true'
        :pageable-button-count='5'>
      <kendo-grid-column
        field="ContactName"
        title="Contact name"
        :width="250">
      </kendo-grid-column>
      <kendo-grid-column
        field="ContactTitle"
        title="Contact title">
      </kendo-grid-column>
      <kendo-grid-column
        field="CompanyName"
        title="Company name">
      </kendo-grid-column>
      <kendo-grid-column
        field="County"
        title="County"
        :width="150">
      </kendo-grid-column>
      </kendo-grid>
    </div>
  </div> 
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1, h2 {
  font-weight: normal;
}

a {
  color: #35495E;
}
</style>
