<!DOCTYPE html>
<html lang="zh">
<head>
  <meta charset="UTF-8">
  <title>公司资产管理系统</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    .asset-gallery img {
      @apply w-24 h-24 object-cover rounded border border-gray-300;
    }
  </style>
</head>
<body class="bg-gray-100 p-6">
  <div class="max-w-5xl mx-auto">
    <h1 class="text-3xl font-bold text-center mb-6">公司资产管理系统</h1>

    <!-- 会计分类 - 流动资产 -->
    <div class="mb-4 bg-white rounded shadow p-4">
      <h2 class="text-xl font-semibold mb-2">流动资产</h2>
      <!-- 单项资产：库存现金 -->
      <div class="mb-2">
        <button onclick="toggleGallery('cash')" class="text-blue-600 underline">库存现金</button>
        <div id="gallery-cash" class="asset-gallery mt-2 hidden flex gap-2 flex-wrap">
          <img src="https://via.placeholder.com/100?text=Cash1" alt="Cash 1">
          <img src="https://via.placeholder.com/100?text=Cash2" alt="Cash 2">
        </div>
      </div>

      <!-- 单项资产：银行存款 -->
      <div class="mb-2">
        <button onclick="toggleGallery('bank')" class="text-blue-600 underline">银行存款</button>
        <div id="gallery-bank" class="asset-gallery mt-2 hidden flex gap-2 flex-wrap">
          <img src="https://via.placeholder.com/100?text=Bank1" alt="Bank 1">
        </div>
      </div>

      <!-- 单项资产：应收账款 -->
      <div class="mb-2">
        <button onclick="toggleGallery('receivables')" class="text-blue-600 underline">应收账款</button>
        <div id="gallery-receivables" class="asset-gallery mt-2 hidden flex gap-2 flex-wrap">
          <img src="https://via.placeholder.com/100?text=Receivable1" alt="Receivable">
        </div>
      </div>
    </div>

    <!-- 会计分类 - 非流动资产 -->
    <div class="mb-4 bg-white rounded shadow p-4">
      <h2 class="text-xl font-semibold mb-2">非流动资产</h2>
      
      <!-- 单项资产：机器设备 -->
      <div class="mb-2">
        <button onclick="toggleGallery('equipment')" class="text-blue-600 underline">机器设备</button>
        <div id="gallery-equipment" class="asset-gallery mt-2 hidden flex gap-2 flex-wrap">
          <img src="https://via.placeholder.com/100?text=Machine1" alt="Machine">
          <img src="https://via.placeholder.com/100?text=Machine2" alt="Machine">
        </div>
      </div>

      <!-- 单项资产：办公楼 -->
      <div class="mb-2">
        <button onclick="toggleGallery('building')" class="text-blue-600 underline">办公楼</button>
        <div id="gallery-building" class="asset-gallery mt-2 hidden flex gap-2 flex-wrap">
          <img src="https://via.placeholder.com/100?text=Building1" alt="Building">
        </div>
      </div>
    </div>
  </div>

  <script>
    function toggleGallery(id) {
      const gallery = document.getElementById('gallery-' + id);
      if (gallery.classList.contains('hidden')) {
        gallery.classList.remove('hidden');
      } else {
        gallery.classList.add('hidden');
      }
    }
  </script>
</body>
</html>
