# 慈善爱心屋

## 学生(Student)

使用学号代表一个学生，且学号不变。

贫困生分为两个等级(poor level)：`一般贫困`和`特别贫困`。这两者在爱心屋兑换物品时没有区分，都可以打三折。

所属学院(college)可能每年会更新——比如有人学生转专业。

## 操作员(operator)

1. 交易操作员(transcation operator)
2. 积分操作员(point operator)
3. 管理员(admin)

## 入库

指任何物品进入慈善爱心屋房间(inventory)内，例如可从仓库(repository)加入。
需要管理员(admin)操作。

## 兑换(redeem)

1. 输入学号，查询列表——可兑换，不可兑换
2. 选择好兑换的物品，通过名称查询物品(item)信息
3. 成功兑换，扣除积分，记录操作员(operator)。

## 物品数量改变

1. 兑换物品
2. 出借物品
3. 归还物品
4. 

如果有老师拿走爱心屋的物品，则会添加一条

## 出借(lend)

- 分类：需要积分，无需积分
- 信息：租借人学号，物品信息，归还日期(deadline)
- 归还日期：根据类型自动选择：跳过双修日；手动设置。
- 操作员(operator)

## 自动填充(auto completion)

- 记录最近几次的交易人员，方便多次交易间填充。
- 记录剪切板历史记录——学号

## 交易记录(Transcation Record)

1. 主体(subject)，学号(student ID)作为ID
2. 备注(note)
3. 物品(item)和数量(amount)
4. 操作员(operator)
5. 时间戳(timestamp)

## 积分改变(Point Change)

1. 交易前积分(point before)，交易后积分(point after)
2. 学号
3. 时间戳(timestamp)
4. 操作员

### 来源

1. 消耗积分兑换物品
2. 消耗积分租借物品
3. 通过志愿活动获得积分
4. 直接修改积分
5. 贫困生每年自动扣分

## 交易(Transcation)

1. 主体(subject)，学号(student ID)作为ID
2. 手机号(phone number)
3. 物品(item),物品价格(point cost)
4. 数量(amount)
5. 线性因子(factor)，用于打折，计算得到结果
6. 操作员(operator)

## 积分(Point)

1. primary key: 学号(student ID)
2. 积分(point)

## 任务分配

计算空闲时间表
