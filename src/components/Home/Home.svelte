<script>
    import AboutBackground from '../../../static/IMG_1280.jpeg'
    import PoetryBackground from '../../../static/IMG_1281.jpeg'
    import BlogBackground from '../../../static/IMG_1284.jpeg'
    import MediaArtBackground from '../../../static/IMG_1285.jpeg'
</script>

<style lang="scss">
    .Home {
        height: 450px;
        text-align: center;
        display: grid;
        grid-template-columns: 33.33% 33.33% 33.33%;
        .Collumn {
            height: 100%;
            margin: 0 10px;
        }
        .Section {
            background-size: cover;
            background-position: center bottom;
            border-radius: 10px;
            transition: 0.3s;
            .Overlay{
                display: flex;
                align-items: center;
                justify-content: center;
                height: 100%;
                border-radius: 10px;
                background-color: rgba(0,0,0,0.15);
                transition: 0.3s;
                h2 {
                    max-width: 50%;
                    color: white;
                    letter-spacing: 1px;
                    font-weight: 300;
                    font-size: 1.5em;
                }
            }
        }
        .Section:hover {
            transform: scale(1.03);
            cursor: pointer;
            .Overlay {
                background-color: rgba(0,0,0,0.35);
            }
        }
        #Blog {
            
        }
        #Media-Art {
            
        }
        #About-Poetry {
            display: grid;
            grid-template-rows: 50% 50%;
            #About {
                margin-bottom: 10px; 
            }
            #Poetry {
                margin-top: 10px;
            }
        }
    }
</style>

<div class="Home">
    <div class="Collumn Section" id="Blog" style="background-image: url({BlogBackground})">
        <a href="blog">
            <div class="Overlay">
                <h2>Blog</h2>
            </div>
        </a>
    </div>
    <div class="Collumn Section" id="Media-Art" style="background-image: url({MediaArtBackground})">
        <a href="media-art">
            <div class="Overlay">
                <h2>Media & Art</h2>
            </div>
        </a>
    </div>
    <div class="Collumn" id="About-Poetry">
        <div class="Section" id="About" style="background-image: url({AboutBackground})" >
            <a href="about">
                <div class="Overlay">
                    <h2>About</h2>
                </div>
            </a>
        </div>
        <div class="Section" id="Poetry" style="background-image: url({PoetryBackground})">
            <a href="poetry">
                <div class="Overlay">
                    <h2>Poetry</h2>
                </div>
            </a>
        </div>
    </div>
</div>