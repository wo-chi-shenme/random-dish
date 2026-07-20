<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>今天吃什么</title>
    
</head>
<body>
    <div class="container">
        <h1>今天吃什么</h1>
        <p class="subtitle">选择困难症终结者</p>
        
        <div class="section-title">选择类型</div>
        <div class="tags" id="typeTags">
            <div class="tag active" data-value="all">全部</div>
            <div class="tag" data-value="中餐">中餐</div>
            <div class="tag" data-value="西餐">西餐</div>
            <div class="tag" data-value="日料">日料</div>
            <div class="tag" data-value="韩餐">韩餐</div>
            <div class="tag" data-value="快餐">快餐</div>
        </div>
        
        <div class="section-title">选择口味</div>
        <div class="tags" id="tasteTags">
            <div class="tag active" data-value="all">全部</div>
            <div class="tag" data-value="辣">辣</div>
            <div class="tag" data-value="清淡">清淡</div>
            <div class="tag" data-value="酸甜">酸甜</div>
            <div class="tag" data-value="咸香">咸香</div>
        </div>
        
        <div class="section-title">选择用餐场景</div>
        <div class="tags" id="sceneTags">
            <div class="tag active" data-value="all">全部</div>
            <div class="tag" data-value="快餐">快餐</div>
            <div class="tag" data-value="正餐">正餐</div>
            <div class="tag" data-value="小吃">小吃</div>
            <div class="tag" data-value="饮品">饮品</div>
        </div>
        
        <button class="btn-random" onclick="getRandomDish()">随机选择</button>
        
        <div class="result" id="result">
            <div class="result-emoji" id="resultEmoji">🍜</div>
            <div class="result-name" id="resultName">红烧牛肉面</div>
            <div class="result-desc" id="resultDesc">热腾腾的面条，浓郁的牛肉汤底，配上劲道的面条</div>
            <div class="result-tags" id="resultTags">#中餐 #咸香 #快餐 #正餐</div>
        </div>
    </div>

    <script>
        const dishes = [
            { name: "红烧牛肉面", emoji: "🍜", type: "中餐", taste: "咸香", scene: "快餐", desc: "热腾腾的面条，浓郁的牛肉汤底" },
            { name: "麻辣火锅", emoji: "🍲", type: "中餐", taste: "辣", scene: "正餐", desc: "热辣辣的锅底，涮着各种食材" },
            { name: "番茄炒蛋", emoji: "🍳", type: "中餐", taste: "酸甜", scene: "正餐", desc: "家常菜，酸甜可口" },
            { name: "酸辣粉", emoji: "🥢", type: "中餐", taste: "辣", scene: "小吃", desc: "酸辣爽滑，开胃解馋" },
            { name: "汉堡包", emoji: "🍔", type: "快餐", taste: "咸香", scene: "快餐", desc: "肉饼香嫩，酱料丰富" },
            { name: "炸鸡", emoji: "🍗", type: "快餐", taste: "咸香", scene: "快餐", desc: "外酥里嫩，香气四溢" },
            { name: "披萨", emoji: "🍕", type: "西餐", taste: "咸香", scene: "正餐", desc: "芝士拉丝，配料丰富" },
            { name: "意大利面", emoji: "🍝", type: "西餐", taste: "咸香", scene: "正餐", desc: "浓郁的番茄肉酱，劲道的面条" },
            { name: "寿司", emoji: "🍣", type: "日料", taste: "清淡", scene: "正餐", desc: "新鲜的鱼生，醋饭香甜" },
            { name: "拉面", emoji: "🍜", type: "日料", taste: "咸香", scene: "正餐", desc: "浓郁的汤底，劲道的面条" },
            { name: "烤肉", emoji: "🥩", type: "韩餐", taste: "咸香", scene: "正餐", desc: "炭火烤制，香气扑鼻" },
            { name: "炸鸡配啤酒", emoji: "🍗", type: "韩餐", taste: "咸香", scene: "正餐", desc: "外酥里嫩，配冰啤酒" },
            { name: "奶茶", emoji: "🧋", type: "快餐", taste: "酸甜", scene: "饮品", desc: "香甜丝滑，解渴神器" },
            { name: "咖啡", emoji: "☕", type: "西餐", taste: "苦", scene: "饮品", desc: "提神醒脑，香气浓郁" },
    if (container.id === "typeTags") selectedType = e.target.dataset.value;
    if (container.id === "tasteTags") selectedTaste = e.target.dataset.value;
        ];
        
    if (container.id === "sceneTags") selectedScene = e.target.dataset.value;
    函数getRandomDish（）{
    让filtered=dishes. filter dish dish=>{
        
    如果（selectedType!==“all”&&dish.Type!==selectedType）返回false；
    如果（selectedTaste!==“all”&&dish.Taste!==selectedTaste）返回false；
    如果（selectedScene!==“all”&&dish.Scene!==selectedScene）返回false；
    返回 true；
                    e.target.classList.add("active");
                    
                    if (container.id === "typeTags") selectedType = e.target.dataset.value;
                    if (container.id === "tasteTags") selectedTaste = e.target.dataset.value;
                    if (container.id === "sceneTags") selectedScene = e.target.dataset.value;
                }
            });
        });
        
        function getRandomDish() {
            let filtered = dishes.filter(dish => {
                if (selectedType !== "all" && dish.type !== selectedType) return false;
                if (selectedTaste !== "all" && dish.taste !== selectedTaste) return false;
                if (selectedScene !== "all" && dish.scene !== selectedScene) return false;
                return true;
            });
            
    if (filtered.length === 0) {
    过滤=碗碟；
            }
            
    const randomIndex = Math.floor(Math.random() * filtered.length);
    const dish = filtered[randomIndex];
            
    document.getElementById("resultEmoji").textContent = dish.emoji;
    document.getElementById("resultName").textContent = dish.name;
    document.getElementById("resultDesc").textContent = dish.desc;
    document.querySelectorAll(".tags").forEach(container => {
            
    container.addEventListener("click", (e) => {
            resultDiv.classList.remove("show");
    if (e.target.classList.contains("tag")) {
            resultDiv.classList.add("show");
        }
    </script>
container.querySelectorAll(".tag").forEach(tag => tag.classList.remove("active"));
</超文本标记语言>
