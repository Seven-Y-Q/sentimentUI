<script>
  // core components
  import Table from "components/Cards/Table.svelte";
  import productList from "../../data/productList.js";
  export let location;

  const headers = [
    "PRODUCT_ID",
    "PRODUCT_NAME",
    "PRODUCT_TYPE",
    "PRINCIPLE_RISK",
    "LIQUIDITY_RISK",
    "COMPLEXITY",
    "PAYBACK_PERIOD",
    "MARKET_RISK",
    "INV_AREA"
  ];

  const data = productList.data;
</script>

<div class="flex flex-wrap mt-4">
  <div class="w-full mb-12 px-4">
    <Table headers={headers} data={data} title="Product" />
  </div>
</div>
