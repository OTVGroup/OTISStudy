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

      .post-content {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: stretch;
        width: 100vw;
        background: black;
        gap: 10px;
        padding: 10px;
      }

      .post-content .post-box {
        flex: 1 1 480px;
        max-width: 30%;
        aspect-ratio: 500/419;
        display: flex;
        background-color: #000000;
        align-content: center;
        justify-content: center;
      }

      .post-content .post-box iframe {
        width: 100%;
        height: 100%;
        border: none;
      }

      @media (max-width: 900px) {
        .post-content .post-box {
          flex: 1 1 420px;
          max-width: 40%;
        }
      }
      @media (max-width: 600px) {
        .post-content .post-box {
          flex: 1 1 360px;
          max-width: 90%;
        }
      }

      .document-pdf {
        width: 90%;
        height: auto;
        margin: auto;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        overflow-x: auto;
        gap: 10px;
      }

      .document-pdf .pdf-filter {
        width: 100%;
        display: flex;
        gap: 10px;
        overflow-x: auto;
        overflow-y: hidden;
        white-space: nowrap;
        scroll-behavior: smooth;
        padding-bottom: 5px;
      }

      .document-pdf .pdf-filter::-webkit-scrollbar {
        height: 5px;
      }

      .document-pdf .pdf-filter::-webkit-scrollbar-thumb {
        background: rgba(0, 0, 0, 0.2);
        border-radius: 999px;
      }

      .document-pdf .pdf-filter .filter-btn {
        flex: 0 0 auto;
        padding: 5px;
        border: 1px solid white;
        border-radius: 5px;
        background: none;
        cursor: pointer;
        font-size: 15px;
        font-weight: 600;
        transition: 0.3s;
        color: white;
      }

      .document-pdf .pdf-filter .filter-btn:hover,
      .document-pdf .pdf-filter .filter-btn.active {
        background: #40e300;
        color: black;
      }

      .document-pdf .pdf-show {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        gap: 10px;
      }

      .document-pdf .pdf-show .show-item {
        position: relative;
        overflow: hidden;
        border-radius: 5px;
        width: clamp(120px, 30%, 360px);
        background: none;
        border: 1px solid #eee;
        transition: 0.3s;
      }

      .document-pdf .pdf-show .show-item:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 25px rgba(0, 0, 0, 0.173);
      }

      .document-pdf .pdf-show .show-item .pdf-img {
        width: 100%;
        display: block;
        object-fit: unset;
        background: none;
      }

      .document-pdf .pdf-show .show-item .pdf-content {
        position: absolute;
        width: 100%;
        bottom: 0;
        background: linear-gradient(
          to bottom,
          rgba(0, 0, 0, 0.4),
          rgb(0, 0, 0)
        );
        display: flex;
        flex-direction: column;
        gap: 5px;
        padding: 10px;
      }

      /* CODE */
      .document-pdf .pdf-show .show-item .pdf-content .content-code {
        width: 100%;
        color: #33cf91;
        font-size: clamp(12px, 5vw, 18px);
        font-weight: bold;
        text-decoration: none;
      }

      /* NAME */
      .document-pdf .pdf-show .show-item .pdf-content .content-name {
        width: 100%;
        color: #31cbd0;
        font-size: clamp(10px, 4vw, 15px);
        line-height: 1.5;
        word-break: break-word;
      }

      /* LINK */
      .document-pdf .pdf-show .show-item .pdf-content .content-link {
        width: 100%;
        color: #242cce;
        text-align: center;
        font-size: clamp(10px, 4vw, 15px);
        font-weight: bold;
        text-decoration: none;
        transition: 0.3s;
      }

      .document-pdf .pdf-show .show-item .pdf-content .content-link:hover {
        color: #ff3c00;
      }

      @media (max-width: 600px) {
        .document-pdf .pdf-show .show-item {
          width: calc(100% - 20px);
        }
      }

      /* Empty */
      .document-pdf .pdf-show .empty-data {
        width: 100%;
        text-align: center;
        padding: 10px;
        background: none;
        border-radius: 14px;
        color: #ffffff;
      }

      .document-pdf .pdf-page {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 10px;
      }

      .document-pdf .pdf-page button {
        width: 30px;
        height: 30px;
        color: white;
        border: 1px solid white;
        border-radius: 50%;
        background: none;
        cursor: pointer;
        font-size: 16px;
        transition: 0.3s;
      }

      .document-pdf .pdf-page button:hover {
        background: #ff4d4f;
      }

      .document-pdf .pdf-page button:disabled {
        opacity: 0.6;
        cursor: not-allowed;
      }

      #pageInfo {
        min-width: 80px;
        text-align: center;
        font-size: 16px;
        font-weight: bold;
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

      <!-- POST -->
      <div class="header introduce view active">
        <strong>NEWS POST</strong>
      </div>
      <div class="post-content introduce view active">
        <div class="post-box">
          <iframe
            src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FOTV.OTISStudy%2Fposts%2Fpfbid0SmL8Loa7RDNQXUEuK54TvBUUWwpCHAJJjDV2Z2GHMdkJxuseQ4PN9GoCfQ7RotGel&show_text=false&width=500"
            style="border: none; overflow: hidden"
            scrolling="no"
            frameborder="0"
            allowfullscreen="true"
            allow="
              autoplay;
              clipboard-write;
              encrypted-media;
              picture-in-picture;
              web-share;
            "
          ></iframe>
        </div>
        <div class="post-box">
          <iframe
            src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FOTV.OTISStudy%2Fposts%2Fpfbid02VvUVqTMzs6SCFrdnaeoLDQDF2eVn6dHbpLn7JLcKFoGZjA9EuuJbcmBHf4FeLtUWl&show_text=false&width=500"
            style="border: none; overflow: hidden"
            scrolling="no"
            frameborder="0"
            allowfullscreen="true"
            allow="
              autoplay;
              clipboard-write;
              encrypted-media;
              picture-in-picture;
              web-share;
            "
          ></iframe>
        </div>
        <div class="post-box">
          <iframe
            src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FOTV.OTISStudy%2Fposts%2Fpfbid0JJyc7bAwCUboPbBe5MiZPfUJxLeucb3aGaeoF1xhwQPJJB8RETVLQZJnZGD5QXq1l&show_text=false&width=500"
            style="border: none; overflow: hidden"
            scrolling="no"
            frameborder="0"
            allowfullscreen="true"
            allow="
              autoplay;
              clipboard-write;
              encrypted-media;
              picture-in-picture;
              web-share;
            "
          ></iframe>
        </div>
      </div>

      <div class="header introduce view active">
        <strong>PLAYLISTS VIDEOS</strong>
      </div>
      <div class="post-content introduce view active" id="playlist"></div>
      <script>
        document.addEventListener("DOMContentLoaded", () => {
          // Danh sách playlist
          const playlistIds = ["PLgWfUHZ9lam-lki8JltbXpxQ5n0V6IFBm"];

          // Playlist muốn bỏ qua
          const excludeIds = [""];

          const container = document.getElementById("playlist");

          const playlists = playlistIds.filter(
            (id) => !excludeIds.includes(id),
          );

          playlists.forEach((playlistId) => {
            container.insertAdjacentHTML(
              "beforeend",
              `
            <div class="post-box">
                <iframe
                    width="100%"
                    height="315"
                    src="https://www.youtube.com/embed/videoseries?list=${playlistId}"
                    title="YouTube playlist"
                    frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
            `,
            );
          });
        });
      </script>

      <div class="document-pdf document view active">
        <div class="pdf-filter">
          <button class="filter-btn active" data-type="all">Tất Cả</button>
          <button class="filter-btn" data-type="BSPG">Lập Trình</button>
          <button class="filter-btn" data-type="BSLG">Ngôn Ngữ</button>
          <button class="filter-btn" data-type="BSTN">Kỹ Thuật</button>
          <button class="filter-btn" data-type="BSET">Điện Tử</button>
          <button class="filter-btn" data-type="BSCC">Sáng Tạo Nội Dung</button>
          <button class="filter-btn" data-type="HSK">HSK</button>
          <button class="filter-btn" data-type="WEB">Web</button>
          <button class="filter-btn" data-type="MATLAB">MatLab</button>
          <button class="filter-btn" data-type="CAD">CAD</button>
          <button class="filter-btn" data-type="SOLID">SolidWorks</button>
          <button class="filter-btn" data-type="SIMU">Simulink</button>
          <button class="filter-btn" data-type="JAVA">Java</button>
          <button class="filter-btn" data-type="TIKTOK">Tik Tok</button>
          <button class="filter-btn" data-type="SHOPEE">Shopee</button>
        </div>

        <!-- Danh sách -->
        <div class="pdf-show" id="list-PDF"></div>

        <!-- Thanh phân trang -->
        <div class="pdf-page">
          <button id="prevPage">
            <i class="fa-solid fa-angle-left"></i>
          </button>

          <span id="pageInfo">1 / 1</span>

          <button id="nextPage">
            <i class="fa-solid fa-angle-right"></i>
          </button>
        </div>
      </div>

      <script>
        const listPDF = document.getElementById("list-PDF");
        const filterBtns = document.querySelectorAll(".filter-btn");
        const pageInfo = document.getElementById("pageInfo");
        const prevPage = document.getElementById("prevPage");
        const nextPage = document.getElementById("nextPage");
        const pdfList = [
          // BSPG - PROGRAMMING
          {
            code: "OTVOS_BSPG01",
            name: "Lập trình Web 2.0",
            type: ["BSPG", "WEB"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/PROGRAMMING/OTVOS_BSPG01.jpg",
            link: "https://drive.google.com/file/d/1V7UpfDzqbyNfutL-VPrfiGumfbuDJpfX/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSPG02",
            name: "50 thuật toán lập trình cho sinh viên IT",
            type: ["BSPG"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/PROGRAMMING/OTVOS_BSPG02.jpg",
            link: "https://drive.google.com/file/d/1EsuEY3MgD2kDy-bG4UUNdwjPbO7G4rQn/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSPG03",
            name: "Tự học Java siêu tốc",
            type: ["BSPG", "JAVA"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/PROGRAMMING/OTVOS_BSPG03.jpg",
            link: "https://drive.google.com/file/d/1winuNRNUMnQ24Y8k7GMEgH32H_qAWsW5/view?usp=drive_link",
          },
          // BSTN - TECHNIQUE
          {
            code: "OTVOS_BSTN01",
            name: "40 mẹo khi sử dụng Solidworks",
            type: ["BSTN", "SOLID"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/TECHNIQUE/OTVOS_BSTN01.jpg",
            link: "https://drive.google.com/file/d/1d-0eDhm635JeFjvYBukNbum4GZSC9aLp/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSTN02",
            name: "200 Bài Tập Luyện CADCAMCNC",
            type: ["BSTN", "CAD"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/TECHNIQUE/OTVOS_BSTN02.jpg",
            link: "https://drive.google.com/file/d/175omK-aiR2PXttsRmG9t0ogC82i7t8_X/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSTN03",
            name: "MATLAB & SIMULINK cho kỹ sư điều khiển tự động",
            type: ["BSTN", "MATLAB", "SIMU"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/TECHNIQUE/OTVOS_BSTN03.jpg",
            link: "https://drive.google.com/file/d/1d-0eDhm635JeFjvYBukNbum4GZSC9aLp/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSTN04",
            name: "Thết Kế Khuôn Với Solidwork",
            type: ["BSTN", "SOLID"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/TECHNIQUE/OTVOS_BSTN04.jpg",
            link: "https://drive.google.com/file/d/175omK-aiR2PXttsRmG9t0ogC82i7t8_X/view?usp=drive_link",
          },
          // BSLG - LANGUAGE
          {
            code: "OTVOS_BSLG01",
            name: "Sách HSK1 Phiên Bản HSK3.0",
            type: ["BSLG", "HSK"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/LANGUAGE/OTVOS_BSLG01.jpg",
            link: "https://drive.google.com/file/d/1rDyfZSI5HJXi1fbh33r53snBmnRg9Sl1/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSLG02",
            name: "33 Bài Luận Trúng Tuyển Đại Học Top Đầu Mỹ",
            type: ["BSLG"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/LANGUAGE/OTVOS_BSLG02.jpg",
            link: "https://drive.google.com/file/d/1ZYyxDvBUv2AyrKDLhLdcDy3vhfrUb4iB/view?usp=drive_link",
          },
          // BSTN - ELECTRONICS
          {
            code: "OTVOS_BSET01",
            name: "Thiết Kế Máy Điện - Thư Viện Cơ Điện Tử",
            type: ["BSET"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/ELECTRONICS/OTVOS_BSET01.jpg",
            link: "https://drive.google.com/file/d/1d-0eDhm635JeFjvYBukNbum4GZSC9aLp/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSET02",
            name: "AC Electrical Circuit Analysis",
            type: ["BSET"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/ELECTRONICS/OTVOS_BSET02.jpg",
            link: "https://drive.google.com/file/d/175omK-aiR2PXttsRmG9t0ogC82i7t8_X/view?usp=drive_link",
          },
          // BSCC - CONTENT CREATOR
          {
            code: "OTVOS_BSCC01",
            name: "Tiktok Policy",
            type: ["BSCC", "TIKTOK"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/CONTENT%20CREATOR/OTVOS_BSCC01.jpg",
            link: "https://drive.google.com/file/d/1PlUfUxn2Yi-ma1t_D9PxYB_AP99XZ7Yj/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSCC02",
            name: "Shopee Map Hoàng Mạnh Cường Topmax",
            type: ["BSCC", "SHOPEE"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/CONTENT%20CREATOR/OTVOS_BSCC02.jpg",
            link: "https://drive.google.com/file/d/1HI-d64tQcO244bphwsMmg_TVhDqOu4bg/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSCC03",
            name: "100 Công Thức Tiêu Đề Video",
            type: ["BSCC"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/CONTENT%20CREATOR/OTVOS_BSCC03.jpg",
            link: "https://drive.google.com/file/d/1HI-d64tQcO244bphwsMmg_TVhDqOu4bg/view?usp=drive_link",
          },
          {
            code: "OTVOS_BSCC04",
            name: "500 Câu Nói Ý Nghĩa Mapevn",
            type: ["BSCC"],
            img: "https://raw.githubusercontent.com/OTVGroup/OTISStudy/main/Folder/CONTENT%20CREATOR/OTVOS_BSCC04.jpg",
            link: "https://drive.google.com/file/d/1gWiD13mEVCBuPC96ymKrOZFajuJ92bZo/view?usp=drive_link",
          },
        ];

        let currentPage = 1;
        const itemPerPage = 3;

        let currentType = "all";
        function getFilteredData() {
          if (currentType === "all") {
            return pdfList;
          }

          return pdfList.filter((item) => {
            return item.type.includes(currentType);
          });
        }

        function renderList() {
          const filteredData = getFilteredData();
          const totalPage = Math.ceil(filteredData.length / itemPerPage);

          /* Fix page */
          if (currentPage > totalPage) {
            currentPage = totalPage || 1;
          }

          /* Start End */
          const start = (currentPage - 1) * itemPerPage;
          const end = start + itemPerPage;
          const currentData = filteredData.slice(start, end);

          /* Empty */
          if (currentData.length === 0) {
            listPDF.innerHTML = `
            <div class="empty-data">
              Không có tài liệu.
            </div>
          `;
          } else {
            listPDF.innerHTML = currentData
              .map(
                (item) => `
            <div class="show-item">
              <img class="pdf-img" src="${item.img}"/>
              <div class="pdf-content">
                <a class="content-code">${item.code}</a>
                <a class="content-name">${item.name}</a>
                <a class="content-link" href="${item.link}" target="_blank">...Xem Chi Tiết</a>
              </div>
            </div>
          `,
              )
              .join("");
          }

          /* Page Info */
          pageInfo.innerHTML = `${currentPage} / ${totalPage || 1}`;

          /* Disable button */
          prevPage.disabled = currentPage <= 1;
          nextPage.disabled = currentPage >= totalPage;
        }

        filterBtns.forEach((btn) => {
          btn.addEventListener("click", () => {
            filterBtns.forEach((b) => {
              b.classList.remove("active");
            });

            btn.classList.add("active");
            currentType = btn.dataset.type;
            currentPage = 1;
            renderList();
          });
        });

        prevPage.addEventListener("click", () => {
          if (currentPage > 1) {
            currentPage--;
            renderList();
          }
        });

        nextPage.addEventListener("click", () => {
          const filteredData = getFilteredData();
          const totalPage = Math.ceil(filteredData.length / itemPerPage);
          if (currentPage < totalPage) {
            currentPage++;
            renderList();
          }
        });

        renderList();
      </script>

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
