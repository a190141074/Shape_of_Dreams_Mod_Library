# 初始添加
::: info
作者：猫妖の舞
:::
## 赠送初始技能/宝石

>==Dew.Contents.dll==
>
>[^Star_Global_StartSkill.OnStartInGame]: 编辑！类！
>
>```C#
>// 1↓，选择编辑类，添加到最上面
>using System;
>using UnityEngine;
>using System.Collections.Generic;
>// 2↓，选择编辑类，放到最下面
>	public static readonly int[] SkillLevel = new int[] { 1, 2, 3 };
>	private static readonly global::System.Random random = new global::System.Random();
>// 3↓选择编辑类，搜索【SelectRarity】，后面有稀有度【Normal普通/High高掉落】，建议改成↓
>			Rarity rarity = lootInstance.SelectRarityHigh();
>// 4↓选择编辑类，这个的原来的，不能删除，下面的添加到这行下面→【Dew.CreateSkillTrigger<SkillTrigger>(skillTrigger, vector, Star_Global_StartSkill.SkillLevel.GetClamped(base.level - 1), base.player, null);】
>			Dew.CreateSkillTrigger<SkillTrigger>(skillTrigger, vector, Star_Global_StartSkill.SkillLevel.GetClamped(base.level - 1), base.player, null);
>
>			// 随机角色技能(不能捡就标记一下就能捡起)
>			List<string> list = new List<string> { "St_D_DisintegratingClaw", "St_D_SalamanderPowder", "St_D_DoubleTap", "St_D_AstridsMasterpiece", "St_D_MercyOfEl", "St_D_Resolve", "St_D_ExoticMatter", "St_D_ConvergencePoint" };
>			Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>(list[Star_Global_StartSkill.random.Next(list.Count)]),vector,1,base.player,null);
>
>			// 单独技能
>			Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Frostbite")vector, 1,base.player, null);// 冻伤
>			//如果要按照局外天赋树的等级,那就把1改成Star_Global_StartSkill.SkillLevel.GetClamped(base.level-1)
>			Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Frostbite")vector,Star_Global_StartSkill.SkillLevel.GetClamped(base.level-1),base.player, null);// 2+冻伤
>
>			// 精华
>			Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Wealth"), vector, 80, base.player, null);// 财富80%
>			Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Momentum"), vector, 80, base.player, null);// 势头80%
>			Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Flow"), vector, 80, base.player, null);// 流动80%
>			Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Virtuousness"), vector, 150, base.player, null);// 高洁150%
>			Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Predation"), vector, 10, base.player, null);// 捕食40%
>			Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Protection"), vector, 200, base.player, null);// 保护200%
>			Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_L_DivineFaith"), vector, 200, base.player, null);// 信仰500%
>```
>
>```C#
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Charcoal"), vector, 10, base.player, null);//[木炭精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Confidence"), vector, 10, base.player, null);//[自信精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Efficiency"), vector, 20, base.player, null);//[效率精华]20%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Guidance"), vector, 10, base.player, null);//[引导精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Lethality"), vector, 10, base.player, null);//[致命精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Quicksilver"), vector, 10, base.player, null);//[水银精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Regeneration"), vector, 10, base.player, null);//[再生精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Sharp"), vector, 10, base.player, null);//[锐利精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Shatter"), vector, 10, base.player, null);//[破碎之精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Sulfur"), vector, 10, base.player, null);//[硫磺之精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Talc"), vector, 10, base.player, null);//[滑石之精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Void"), vector, 10, base.player, null);//[虚空精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Wind"), vector, 10, base.player, null);//[风之精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_C_Vengeance"), vector, 10, base.player, null);//[复仇精华]10%[白]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Blade"), vector, 10, base.player, null);//[利刃精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Bleak"), vector, 10, base.player, null);//[荒凉之精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Celestial"), vector, 10, base.player, null);//[天体精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Contempt"), vector, 10, base.player, null);//[蔑视精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Dusk"), vector, 10, base.player, null);//[黄昏精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Flow"), vector, 40, base.player, null);//[流动的精华]40%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Frost"), vector, 10, base.player, null);//[霜冻精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Glaciate"), vector, 100, base.player, null);//[冰封精华]100%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Insatiable"), vector, 10, base.player, null);//[贪食精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Momentum"), vector, 40, base.player, null);//[势头精华]40%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_NightSky"), vector, 10, base.player, null);//[夜空精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Scorched"), vector, 10, base.player, null);//[烧灼之精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Rigidity"), vector, 10, base.player, null);//[刚毅精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Spiral"), vector, 10, base.player, null);//[漩涡精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Wealth"), vector, 100, base.player, null);//[财富精华]100%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_R_Wound"), vector, 10, base.player, null);//[创伤精华]10%[蓝]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Clemency"), vector, 10, base.player, null);//[宽恕精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Direness"), vector, 10, base.player, null);//[绝境精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Fever"), vector, 10, base.player, null);//[热病精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Flexibility"), vector, 10, base.player, null);//[灵活性精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Insight"), vector, 10, base.player, null);//[洞察之精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Metal"), vector, 100, base.player, null);//[金属精华]100%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Might"), vector, 10, base.player, null);//[巨人精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Omega"), vector, 10, base.player, null);//[终极精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Overload"), vector, 10, base.player, null);//[过载之精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Pain"), vector, 10, base.player, null);//[苦痛精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Predation"), vector, 40, base.player, null);//[掠食之精华]40%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Protection"), vector, 200, base.player, null);//[保护之精华]200%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Thunder"), vector, 10, base.player, null);//[雷霆精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Twilight"), vector, 10, base.player, null);//[暮光之精华]10%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_E_Virtuousness"), vector, 150, base.player, null);//[高洁之精华]150%[紫]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_L_DivineFaith"), vector, 500, base.player, null);//[神圣信仰]500%[红]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_L_Embertail"), vector, 10, base.player, null);//[火焰尾巴]10%[红]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_L_GlacialCore"), vector, 10, base.player, null);//[冰川之核]10%[红]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_L_Paranoia"), vector, 100, base.player, null);//[偏执精华]100%[红]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_L_Perfect"), vector, 10, base.player, null);//[完美]10%[红]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_L_PureWhite"), vector, 10, base.player, null);//[纯白]10%[红]
>Dew.CreateGem<Gem>(DewResources.GetByShortTypeName<Gem>("Gem_L_SolarEye"), vector, 10, base.player, null);//[太阳之眼]10%[红]
>```
>
>```C#
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_BackStep")vector, 1,base.player, null);//[后退]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_BeamOfLight")vector, 1,base.player, null);//[光之射线]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_DarkBolt")vector, 1,base.player, null);//[暗影箭]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_DarkSpear")vector, 1,base.player, null);//[暗影之矛]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_GlacialStomp")vector, 1,base.player, null);//[冰川践踏]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_IceBlock")vector, 1,base.player, null);//[冰盾]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_IceClaw")vector, 1,base.player, null);//[冰爪]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_PressurePoint")vector, 1,base.player, null);//[压力释放]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_Purgatory")vector, 1,base.player, null);//[炼狱]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_Starfall")vector, 1,base.player, null);//[星陨]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_Whirlwind")vector, 1,base.player, null);//[旋转旋风]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_ShadowWalk")vector, 1,base.player, null);//[影步]1-1级[白]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_BlackArbalest")vector, 1,base.player, null);//[黑色弩炮]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Chomp")vector, 1,base.player, null);//[撕咬]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_FlamingWhip")vector, 1,base.player, null);//[炽焰鞭]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Frostbite")vector, 1,base.player, null);//[冻伤]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_GlacialHammer")vector, 1,base.player, null);//[冰川之锤]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_GreatFrostSword")vector, 1,base.player, null);//[霜冻巨剑]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Ignite")vector, 1,base.player, null);//[点燃]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_PillarOfFlame")vector, 1,base.player, null);//[烈焰之柱]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_RepulsiveShield")vector, 1,base.player, null);//[反冲之盾]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Scattershot")vector, 1,base.player, null);//[散射]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Smite")vector, 1,base.player, null);//[雷击]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_StaticDischarge")vector, 1,base.player, null);//[静电释放]1-1级[蓝]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_E_AntiGravity")vector, 1,base.player, null);//[反重力]1-1级[紫]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_E_Blink")vector, 1,base.player, null);//[闪现]1-1级[紫]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_E_ChainLightning")vector, 1,base.player, null);//[连锁闪电]1-1级[紫]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_E_ClutchesOfMalice")vector, 1,base.player, null);//[恶意之爪]1-1级[紫]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_E_FlameJet")vector, 1,base.player, null);//[火焰喷射]1-1级[紫]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_E_Rewind")vector, 1,base.player, null);//[倒带]1-1级[紫]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_E_SearingCharge")vector, 1,base.player, null);//[炽热冲锋]1-1级[紫]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_E_UmbralEdge")vector, 1,base.player, null);//[暗影之刃]1-1级[紫]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_E_WinterDive")vector, 1,base.player, null);//[冬季跳跃]1-1级[紫]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_L_Hysteria")vector, 1,base.player, null);//[癫狂]1-1级[红]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_L_MentalCorruption")vector, 1,base.player, null);//[精神腐蚀]1-1级[红]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_L_Multishot")vector, 1,base.player, null);//[箭雨]1-1级[红]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_L_ShoutOfOblivion")vector, 1,base.player, null);//[遗忘之吼]1-1级[红]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_L_WorldCracker")vector, 1,base.player, null);//[世界破坏者]1-1级[红]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_M_NimbleDodge")vector, 1,base.player, null);//[灵巧闪避]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_Q_HandCannon")vector, 1,base.player, null);//[手炮]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_Q_IncendiaryRounds")vector, 1,base.player, null);//[燃烧弹装填]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_QuickTrigger")vector, 1,base.player, null);//[快速扳机]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_PrecisionShot")vector, 1,base.player, null);//[精准射击]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_D_SalamanderPowder")vector, 1,base.player, null);//[火蜥蜴粉末]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_D_DoubleTap")vector, 1,base.player, null);//[双击]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_M_FastFeet")vector, 1,base.player, null);//[迅捷步伐]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_Q_Lunge")vector, 1,base.player, null);//[突刺冲锋]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_Q_Fleche")vector, 1,base.player, null);//[闪击]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_UnbreakableDetermination")vector, 1,base.player, null);//[坚不可摧的意志]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Parry")vector, 1,base.player, null);//[招架]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_D_AstridsMasterpiece")vector, 1,base.player, null);//[阿斯特丽德的杰作]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_M_Flicker")vector, 1,base.player, null);//[闪烁]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_Q_EtherealInfluence")vector, 1,base.player, null);//[以太的影响]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_Q_SuperNova")vector, 1,base.player, null);//[超新星]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Cataclysm")vector, 1,base.player, null);//[大灾变]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_Tranquility")vector, 1,base.player, null);//[平静]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_D_ExoticMatter")vector, 1,base.player, null);//[异种物质]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_D_ConvergencePoint")vector, 1,base.player, null);//[汇聚之星]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_M_Charge")vector, 1,base.player, null);//[重甲打击]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_Q_CruelSun")vector, 1,base.player, null);//[残酷太阳]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_Q_Discipline")vector, 1,base.player, null);//[纪律]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_SanctuaryOfEl")vector, 1,base.player, null);//[埃尔的圣域]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_D_Resolve")vector, 1,base.player, null);//[决意]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_D_MercyOfEl")vector, 1,base.player, null);//[艾尔的仁慈]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_M_FeatheryDash")vector, 1,base.player, null);//[羽毛飞舞]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_Q_GoldenBurst")vector, 1,base.player, null);//[金色爆发]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_R_DangerousTheory")vector, 1,base.player, null);//[危险理论]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_D_DisintegratingClaw")vector, 1,base.player, null);//[分解之爪]1-1级[金]
>Dew.CreateSkillTrigger<SkillTrigger>(DewResources.GetByShortTypeName<SkillTrigger>("St_C_Sneeze")vector, 1,base.player, null);//[喷嚏]1-1级[灰]
>```
>
>
