<script>
    export let posts
</script>

<style type="text/scss">
    .Blog-Cards {
        display: grid;
        grid-template-columns: 20% 20% 20% 20% 20%;
        .Card {
            margin: 10px;
            .Card-Picture {
                .Card-Picture-Overlay {
                    img {

                    }
                    p {

                    }
                }
            }
            .Card-title {
                h4 {

                }
            }
        }
    }
</style>

<div class="Blog-Cards">
    {#each posts as post, index}
        <div class="Card">
            <a href="blog/{post.fields.slug}">
                <div class="Card-Picture">
                    <div class="Card-Picture-Overlay">
                        <img src={post.pic} alt="Blog Picture">
                        <!--p>{post.description}</p-->
                    </div>
                </div>
            </a>
            <div class="Card-Title">
                <h4>{post.title}</h4>
            </div>
        </div>
    {/each}
</div>