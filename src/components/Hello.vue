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
        :transportRead="'https://demos.telerik.com/kendo-ui/service/Northwind.svc/Orders'"
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
        field="OrderID"
        title="Order-id"
        :width="250">
      </kendo-grid-column>
      <kendo-grid-column
        field="OrderDate"
        title="Order date">
      </kendo-grid-column>
      <kendo-grid-column
        field="Freight"
        title="Freight">
      </kendo-grid-column>
      <kendo-grid-column
        field="ShipCity"
        title="Ship city">
      </kendo-grid-column>
      <kendo-grid-column
        field="ShipRegion"
        title="Ship region">
      </kendo-grid-column>
      <kendo-grid-column
        field="ShipPostalCode"
        title="Ship postal code">
      </kendo-grid-column>
      <kendo-grid-column
        field="ShipCountry"
        title="Ship country">
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
