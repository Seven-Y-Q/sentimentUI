<script>
  // core components
  import Table from "components/Cards/Table.svelte";
  import commentsByArticle from "../../data/commentsByArticle.js";
  export let location;

  const headers = [
    "comment_id",
    "msg_id",
    "ref_prod",
    "open_id",
    "content",
    "sentiment_score",
    "sentiment_magnitude"
  ];

  const data = commentsByArticle.data;
</script>

<div class="flex flex-wrap mt-4">
  <div class="w-full mb-12 px-4">
    <Table headers={headers} data={data} title="Comments by Article" />
  </div>
</div>
