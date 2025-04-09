# 禁用精华/记忆表
::: info
作者：猫妖の舞
:::

## 删除精华

> ==Dew.Core.dll==
>
> [^Loot_Gem.SelectGemAndQuality]: 编辑方法/类
>
> ```C#
> //↓去掉开头的//就是禁用
> HashSet<string> pool = NetworkedManagerBase<LootManager>.instance.poolGemsByRarity[**rarity**];
> //pool.Remove("Gem_C_Charcoal");//木炭精华
> //pool.Remove("Gem_C_Confidence");//自信精华
> //pool.Remove("Gem_C_Efficiency");//效率精华
> //pool.Remove("Gem_C_Guidance");//引导精华
> //pool.Remove("Gem_C_Lethality");//致命精华
> //pool.Remove("Gem_C_Quicksilver");//水银精华
> //pool.Remove("Gem_C_Regeneration");//再生精华
> //pool.Remove("Gem_C_Sharp");//锐利精华
> //pool.Remove("Gem_C_Shatter");//破碎之精华
> //pool.Remove("Gem_C_Sulfur");//硫磺之精华
> //pool.Remove("Gem_C_Talc");//滑石之精华
> //pool.Remove("Gem_C_Void");//虚空精华
> //pool.Remove("Gem_C_Wind");//风之精华
> //pool.Remove("Gem_C_Vengeance");//复仇精华
> //pool.Remove("Gem_R_Blade");//利刃精华
> //pool.Remove("Gem_R_Bleak");//荒凉之精华
> //pool.Remove("Gem_R_Celestial");//天体精华
> //pool.Remove("Gem_R_Contempt");//蔑视精华
> //pool.Remove("Gem_R_Dusk");//黄昏精华
> //pool.Remove("Gem_R_Flow");//流动的精华
> //pool.Remove("Gem_R_Frost");//霜冻精华
> //pool.Remove("Gem_R_Glaciate");//冰封精华
> //pool.Remove("Gem_R_Insatiable");//贪食精华
> //pool.Remove("Gem_R_Momentum");//势头精华
> //pool.Remove("Gem_R_NightSky");//夜空精华
> //pool.Remove("Gem_R_Scorched");//烧灼之精华
> //pool.Remove("Gem_R_Rigidity");//刚毅精华
> //pool.Remove("Gem_R_Spiral");//漩涡精华
> //pool.Remove("Gem_R_Wealth");//财富精华
> //pool.Remove("Gem_R_Wound");//创伤精华
> //pool.Remove("Gem_E_Clemency");//宽恕精华
> //pool.Remove("Gem_E_Direness");//绝境精华
> //pool.Remove("Gem_E_Fever");//热病精华
> //pool.Remove("Gem_E_Flexibility");//灵活性精华
> //pool.Remove("Gem_E_Insight");//洞察之精华
> //pool.Remove("Gem_E_Metal");//金属精华
> //pool.Remove("Gem_E_Might");//巨人精华
> //pool.Remove("Gem_E_Omega");//终极精华
> //pool.Remove("Gem_E_Overload");//过载之精华
> //pool.Remove("Gem_E_Pain");//苦痛精华
> //pool.Remove("Gem_E_Predation");//掠食之精华
> //pool.Remove("Gem_E_Protection");//保护之精华
> //pool.Remove("Gem_E_Thunder");//雷霆精华
> //pool.Remove("Gem_E_Twilight");//暮光之精华
> //pool.Remove("Gem_E_Virtuousness");//高洁之精华
> //pool.Remove("Gem_L_DivineFaith");//神圣信仰
> //pool.Remove("Gem_L_Embertail");//火焰尾巴
> //pool.Remove("Gem_L_GlacialCore");//冰川之核
> //pool.Remove("Gem_L_Paranoia");//偏执精华
> //pool.Remove("Gem_L_Perfect");//完美
> //pool.Remove("Gem_L_PureWhite");//纯白
> //pool.Remove("Gem_L_SolarEye");//太阳之眼
> ```
>
> 1

## 删除技能

> ==Dew.Core.dll==
>
> [^Loot_Skill.SelectSkillAndLevel]: 编辑方法
>
> ```c#
> //↓去掉开头的//就是禁用
> HashSet<string> pool = NetworkedManagerBase<LootManager>.instance.poolSkillsByRarity[rarity];
> //pool.Remove("St_C_BackStep");//后退
> //pool.Remove("St_C_BeamOfLight");//光之射线
> //pool.Remove("St_C_DarkBolt");//暗影箭
> //pool.Remove("St_C_DarkSpear");//暗影之矛
> //pool.Remove("St_C_GlacialStomp");//冰川践踏
> //pool.Remove("St_C_IceBlock");//冰盾
> //pool.Remove("St_C_IceClaw");//冰爪
> //pool.Remove("St_C_PressurePoint");//压力释放
> //pool.Remove("St_C_Purgatory");//炼狱
> //pool.Remove("St_C_Starfall");//星陨
> //pool.Remove("St_C_Whirlwind");//旋转旋风
> //pool.Remove("St_R_ShadowWalk");//影步
> //pool.Remove("St_R_BlackArbalest");//黑色弩炮
> //pool.Remove("St_R_Chomp");//撕咬
> //pool.Remove("St_R_FlamingWhip");//炽焰鞭
> //pool.Remove("St_R_Frostbite");//冻伤
> //pool.Remove("St_R_GlacialHammer");//冰川之锤
> //pool.Remove("St_R_GreatFrostSword");//霜冻巨剑
> //pool.Remove("St_R_Ignite");//点燃
> //pool.Remove("St_R_PillarOfFlame");//烈焰之柱
> //pool.Remove("St_R_RepulsiveShield");//反冲之盾
> //pool.Remove("St_R_Scattershot");//散射
> //pool.Remove("St_R_Smite");//雷击
> //pool.Remove("St_R_StaticDischarge");//静电释放
> //pool.Remove("St_E_AntiGravity");//反重力
> //pool.Remove("St_E_Blink");//闪现
> //pool.Remove("St_E_ChainLightning");//连锁闪电
> //pool.Remove("St_E_ClutchesOfMalice");//恶意之爪
> //pool.Remove("St_E_FlameJet");//火焰喷射
> //pool.Remove("St_E_Rewind");//倒带
> //pool.Remove("St_E_SearingCharge");//炽热冲锋
> //pool.Remove("St_E_UmbralEdge");//暗影之刃
> //pool.Remove("St_E_WinterDive");//冬季跳跃
> //pool.Remove("St_L_Hysteria");//癫狂
> //pool.Remove("St_L_MentalCorruption");//精神腐蚀
> //pool.Remove("St_L_Multishot");//箭雨
> //pool.Remove("St_L_ShoutOfOblivion");//遗忘之吼
> //pool.Remove("St_L_WorldCracker");//世界破坏者
> //pool.Remove("St_M_NimbleDodge");//灵巧闪避
> //pool.Remove("St_Q_HandCannon");//手炮
> //pool.Remove("St_Q_IncendiaryRounds");//燃烧弹装填
> //pool.Remove("St_R_QuickTrigger");//快速扳机
> //pool.Remove("St_R_PrecisionShot");//精准射击
> //pool.Remove("St_D_SalamanderPowder");//火蜥蜴粉末
> //pool.Remove("St_D_DoubleTap");//双击
> //pool.Remove("St_M_FastFeet");//迅捷步伐
> //pool.Remove("St_Q_Lunge");//突刺冲锋
> //pool.Remove("St_Q_Fleche");//闪击
> //pool.Remove("St_R_UnbreakableDetermination");//坚不可摧的意志
> //pool.Remove("St_R_Parry");//招架
> //pool.Remove("St_D_AstridsMasterpiece");//阿斯特丽德的杰作
> //pool.Remove("St_M_Flicker");//闪烁
> //pool.Remove("St_Q_EtherealInfluence");//以太的影响
> //pool.Remove("St_Q_SuperNova");//超新星
> //pool.Remove("St_R_Cataclysm");//大灾变
> //pool.Remove("St_R_Tranquility");//平静
> //pool.Remove("St_D_ExoticMatter");//异种物质
> //pool.Remove("St_D_ConvergencePoint");//汇聚之星
> //pool.Remove("St_M_Charge");//重甲打击
> //pool.Remove("St_Q_CruelSun");//残酷太阳
> //pool.Remove("St_Q_Discipline");//纪律
> //pool.Remove("St_R_SanctuaryOfEl");//埃尔的圣域
> //pool.Remove("St_D_Resolve");//决意
> //pool.Remove("St_D_MercyOfEl");//艾尔的仁慈
> //pool.Remove("St_M_FeatheryDash");//羽毛飞舞
> //pool.Remove("St_Q_GoldenBurst");//金色爆发
> //pool.Remove("St_R_DangerousTheory");//危险理论
> //pool.Remove("St_D_DisintegratingClaw");//分解之爪
> ```