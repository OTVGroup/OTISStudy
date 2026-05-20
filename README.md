<html lang="vi">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="Khởi Đầu Nhỏ, Thành Công Lớn!" />
    <meta name="author" content="OTISStudy" />
    <meta
      name="image"
      content="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Picture/Avatar%20-%20OTISStudy.png"
    />
    <title>OTISStudy | Khởi Đầu Nhỏ, Thành Công Lớn!</title>
    <link
      rel="icon"
      type="image/jpeg"
      href="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Picture/Avatar%20-%20OTISStudy.png"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
    />
    <!-- Google Analytics -->
    <script
      async
      src="https://www.googletagmanager.com/gtag/js?id=G-H6LM2XKZTS"
    ></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag() {
        dataLayer.push(arguments);
      }
      gtag("js", new Date());
      gtag("config", "G-H6LM2XKZTS");
    </script>
    <style>
      html {
        overflow: -moz-scrollbars-none; /* Firefox cũ */
        scrollbar-width: none; /* Firefox mới */
        scroll-behavior: smooth; /* Cuộn mượt */
      }
      ::-webkit-scrollbar {
        width: 0 !important; /* 🎯 Không chiếm không gian */
        height: 0 !important;
        display: none !important; /* 🎯 Ẩn hoàn toàn */
      }
      /* 🎯 Đảm bảo không có padding/margin cho thanh cuộn */
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      body {
        font-family: "Segoe UI", sans-serif;
        background-color: #000000;
        color: #ffffff;
      }

      /* Header */
      .body-top {
        width: 100vw;
        height: 75px;
        background-color: #000000;
        position: fixed;
        top: 0;
        left: 0;
        display: flex; /* dùng flexbox để căn giữa nội dung */
        align-items: center;
        align-content: center;
        justify-content: center;
      }

      .body-top .img {
        width: min(100px, 10%);
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .body-top .img img {
        height: 60px;
        border-radius: 50%;
        margin: auto;
        box-shadow:
          0 0 10px rgb(226, 226, 226),
          0 0 10px rgb(250, 250, 250);
      }

      .menu {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100%;
        width: max(80%, 100% - 200px);
      }

      .menu label {
        width: max(120px, 30%);
        text-align: center;
        padding: 0px 5px;
      }

      .menu label a {
        width: 100%;
        font-size: clamp(15px, 1.8vw, 24px);
        font-family: "Montserrat", sans-serif;
        letter-spacing: 1px;
        text-align: center;
        padding: 0px 5px;
        color: #ffffff;
        font-weight: 600;
        text-decoration: none;
      }

      .menu label a:hover {
        color: rgba(123, 226, 255, 0.867);
      }

      @media (max-width: 600px) {
        .body-top .img {
          display: none;
        }

        .menu {
          width: 100%;
        }

        .menu label {
          width: 30%;
        }

        .menu label a {
          font-size: 15px;
        }
      }

      .body-bottom {
        position: absolute;
        top: 80px;
        left: 50%;
        transform: translateX(-50%); /* dịch tâm khối về chính giữa */

        width: 100vw;
        min-width: 400px;
        height: calc(100vh - 80px);
        overflow-x: scroll;

        font-family: "Segoe UI", sans-serif;
        background-color: #000000;
        color: #ffffff;
      }

      .header {
        width: 100vw;
        padding: 10px 20px 15px 20px;
        min-width: 400px;
        height: auto;
        display: flex;
        background-color: #000000;
        border-top: 2px solid #ffffff;
        align-items: center;
        align-content: center;
        justify-items: center;
        justify-content: center;
      }

      .header strong {
        font-size: clamp(14px, 1.8vw, 24px);
        color: #ffffff;
        height: 28px;
        text-shadow:
          0 0 2px rgba(255, 255, 255, 0.748),
          0 0 5px rgb(122, 177, 255);
      }

      .panel {
        width: 100vw;
        aspect-ratio: 1920/360;
        margin: 0 auto;
      }

      /* VIDEO REVIEW */
      .video-container {
        width: 100%;
        height: auto;
        min-width: 320px;
        max-height: calc(100dvh - 80px);
        aspect-ratio: 16 / 9;
        margin: 0 auto;
        border-radius: 5px;
        display: flex;
        background: #000000;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .video-content {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: stretch;
        width: 100vw;
        background: black;
        gap: 10px;
        padding: 10px;
      }

      .video-content .video-box {
        flex: 1 1 480px;
        max-width: 50%;
        aspect-ratio: 16/9;
        background-color: #000000;
      }

      .video-content .video-box iframe {
        width: 100%;
        height: 100%;
        border: none;
      }

      @media (max-width: 900px) {
        .video-content .video-box {
          flex: 1 1 420px;
        }
      }

      @media (max-width: 600px) {
        .video-content .video-box {
          flex: 1 1 360px;
          max-width: 100%;
        }
      }

      .body-bottom .view {
        display: none;
      }

      .body-bottom .view.active {
        display: flex;
      }

      /* FOOTER */
      .footer {
        width: 100%;
        height: auto;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        background: #2a2a2a;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
      }

      .footer .f-left,
      .footer .f-center,
      .footer .f-right {
        min-width: 360px;
        flex: 1;
        height: min-content;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .footer span {
        width: 100%;
        height: 30px;
        min-width: 300px;
        margin: 0;
        display: flex;
        padding: 0 15px;
        font-size: 18px;
        font-weight: 600;
        color: white;
        background-color: rgba(67, 67, 67, 0.708);
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        align-items: left;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .footer .f-content {
        width: 100%;
        height: fit-content;
        min-height: 30px;
        min-width: 300px;
        margin: 0;
        display: flex;
        padding: 5px 10px;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .footer .f-content a {
        color: rgb(195, 195, 195);
        width: 100%;
        display: flex;
        height: 20px;
        font-size: 15px;
        text-decoration: none;
      }

      .footer .f-content a i {
        margin-right: 3px;
        width: 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        justify-items: center;
      }

      .footer .f-content a:hover,
      .footer .f-content a:active {
        color: #ededed;
      }

      @media (max-width: 990px) {
        .footer .f-left,
        .footer .f-center {
          width: calc(100% / 2);
        }

        .footer .f-right {
          width: 100%;
        }
      }

      @media (max-width: 660px) {
        .footer .f-left,
        .footer .f-center,
        .footer .f-right {
          width: 100%;
        }
      }

      /* COPYRIGHT */
      .copyright {
        font-size: 15px;
        text-align: center;
        opacity: 0.8;
        line-height: 1.5;
        color: #c1c1c1; /* xám dịu */
      }
    </style>
  </head>
  <body>
    <!-- Header Logo -->
    <div class="body-top">
      <div class="img">
        <img
          src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Picture/Avatar%20-%20OTISStudy.png"
          alt="Background"
        />
      </div>
      <div class="menu">
        <label data-target="introduce"><a>GIỚI THIỆU</a></label>
        <label data-target="document"><a>TÀI LIỆU</a></label>
        <label data-target="course"><a>KHÓA HỌC</a></label>
      </div>
      <div class="img">
        <img
          src="https://raw.githubusercontent.com/OTVGroup/OTVGroup/main/Picture/Avatar%20-%20OTISStudy.png"
          alt="Background"
        />
      </div>
    </div>

    <div class="body-bottom">
      <!-- VIDEO -->
      <div class="video-container introduce view active"></div>
      <script>
        const fixedVideo = "XQPTf29gYnQ";
        let player;

        // load youtube api
        function loadYouTubeAPI() {
          return new Promise((resolve) => {
            if (window.YT && YT.Player) return resolve();

            const tag = document.createElement("script");
            tag.src = "https://www.youtube.com/iframe_api";
            document.body.appendChild(tag);

            window.onYouTubeIframeAPIReady = () => resolve();
          });
        }

        function createPlayer() {
          const container = document.querySelector(".video-container");

          player = new YT.Player(container, {
            videoId: fixedVideo,
            playerVars: {
              autoplay: 1,
              mute: 1,
              controls: 0, // hiện control
              rel: 1,
              modestbranding: 0,
              loop: 1,
              playlist: fixedVideo, // bắt buộc để loop
              fs: 0, // bỏ fullscreen
              iv_load_policy: 3, // bỏ annotation
            },
            events: {
              onReady: (e) => e.target.playVideo(),
            },
          });
        }

        async function init() {
          await loadYouTubeAPI();
          createPlayer();
        }

        init();
      </script>

      <!-- Panel -->
      <img
        src="https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Panel/OTISStudy.png"
        alt="Panel/OTISStudy"
        class="panel introduce view active"
      />

      <div class="header introduce view active">
        <strong>OTISStudy - Khởi Đầu Nhỏ, Thành Công Lớn!</strong>
      </div>

      <div class="header introduce view active">
        <strong>NEW POST</strong>
      </div>
      <div class="video-content introduce view active" id="playlist"></div>
      <script>
        document.addEventListener("DOMContentLoaded", async () => {
          const channelId = "UCyHIlctEZtevylteyDA5ihA";
          const excludeIds = ["bOQM5JftO7s", "6Nn4E6OtKxo", "FFmTEOPVqBc"];

          const container = document.getElementById("playlist");

          const url =
            `https://api.rss2json.com/v1/api.json?rss_url=` +
            encodeURIComponent(
              `https://www.youtube.com/feeds/videos.xml?channel_id=${channelId}`,
            );

          try {
            const res = await fetch(url);
            const data = await res.json();

            const videos = data.items
              .filter(
                (video) => !excludeIds.includes(video.link.split("v=")[1]),
              )
              .slice(0, 6);

            videos.forEach((video) => {
              const videoId = video.link.split("v=")[1];

              container.insertAdjacentHTML(
                "beforeend",
                `
                        <div class="video-box">
                            <iframe
                                width="100%"
                                height="315"
                                src="https://www.youtube.com/embed/${videoId}"
                                frameborder="0"
                                allowfullscreen>
                            </iframe>
                        </div>
                        `,
              );
            });
          } catch (err) {
            console.error(err);
          }
        });
      </script>

      <div class="introduce"></div>

      <!-- Copyright -->
      <div class="copyright">
        © <span id="year"></span> OTISStudy. Tất cả các quyền được bảo lưu.
      </div>
    </div>

    <script>
      const labels = document.querySelectorAll(".menu label");
      labels.forEach((label) => {
        label.addEventListener("click", () => {
          const target = label.dataset.target;
          // active menu
          labels.forEach((l) => l.classList.remove("active"));
          label.classList.add("active");
          // show nội dung
          document
            .querySelectorAll(".view")
            .forEach((v) => v.classList.remove("active"));
          document
            .querySelectorAll("." + target)
            .forEach((v) => v.classList.add("active"));
        });
      });
    </script>
  </body>
</html>
