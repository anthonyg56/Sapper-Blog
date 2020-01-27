<script>
    export let post
    export let article
</script>

<style type="text/scss">
    .Blog-Post {
        height: 100%;
        .Picture {

        }
        .Text {
            h3 {

            }
            h4 {

            }
            p {

            }
        }
    }
</style>

<div class="Blog-Post">
    <div class="Picture">
        <img src={post.pic} alt="">
    </div>
    <div class="Text">
        <h3>{post.title}</h3>
        <h4>{post.date}</h4>
    </div>
    <div>
        {@html article}
    </div>
</div>