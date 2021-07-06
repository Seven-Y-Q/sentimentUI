<script>
  // core components
  import Table from "components/Cards/Table.svelte";
  import followers from "../../data/followers.js";
  export let location;

  const headers = [
    "OPEN_ID",
    "NICK_NAME",
    "LANG",
    "SEX",
    "COUNTRY",
    "CITY",
    "BIND_STATUS",
    "SUBSCRIBE_STATUS",
    "SUBSCRIBE_SCENE",
    "GROUP_ID",
    "TAGID_LIST",
    "UNION_ID",
    "REMARK",
    "SUBSCRIBE_TIME",
  ];

  const data = followers.data;
</script>

<div class="flex flex-wrap mt-4">
  <div class="w-full mb-12 px-4">
    <Table headers={headers} data={data} title="Followers" />
  </div>
</div>
