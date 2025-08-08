# 为测试集添加高斯噪声攻击（例如：30%测试样本被攻击）
num_test_attack = int(len(testset) * 0.3)
test_attack_indices = set(random.sample(range(len(testset)), num_test_attack))
test_clean_indices = set(range(len(testset))) - test_attack_indices

# 创建带噪声的测试集
testset_noisy = NoisyCIFAR10Dataset(testset, test_attack_indices, noise_level=4.5)

# 创建 DataLoader
testloader_noisy = DataLoader(testset_noisy, batch_size=64, shuffle=False)

# 可视化测试集中受攻击的样本
show_images(testset_noisy, test_attack_indices, "Attacked Test Samples")
show_images(testset_noisy, test_clean_indices, "Clean Test Samples")

# 拆分干净与受攻击测试集
test_attack_subset = Subset(testset_noisy, list(test_attack_indices))
test_clean_subset = Subset(testset_noisy, list(test_clean_indices))

# 创建对应的 DataLoader
attackTestloader = DataLoader(test_attack_subset, batch_size=64, shuffle=False)
cleanTestloader = DataLoader(test_clean_subset, batch_size=64, shuffle=False)

# 打印测试子集大小
print(f"Test - Attack: {len(test_attack_subset)}, Clean: {len(test_clean_subset)}")
