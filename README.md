# Lua
num = {1,2,3,4,5,6,7,8,9}
obj = {}
function CreatTable()
    for key, value in ipairs(num) do
        obj = UguiAddChid(gameObject, CardItemPrefab, "Card"..value..'_' ..key  );
        SetCardImg(obj.transform, value);
        AddEvent(obj);
        AddColor(value)
        table.insert(obj, {cardNums = value, cardObj = obj})
    end
    FirstShowCard(#majiangobj)
end
--一种两层表的写法
function ReadTable()
     for key, value in ipairs(obj) do
        value.cardNums = 10
        value.cardObj.transfrom.postion = Vector3.zero
     end
end
