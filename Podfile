source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '9.0'

def common_pods
  pod 'RealmSwift'
  pod 'AMWaveTransition', '~> 0.5'
  pod 'AHKActionSheet', '~> 0.5'
  pod 'pop', '~> 1.0'
  pod 'AMPopTip', '~> 0.7'
  pod 'UICountingLabel', '~> 1.2'
  pod 'JTCalendar', git: 'https://github.com/andreamazz/JTCalendar', branch: 'develop'
  pod 'BAFluidView', '~> 0.1.6'
  pod 'BubbleTransition', '~> 1.0.0'
  pod 'SwiftDate', '~> 1.2'
end

target 'Gulps' do
  common_pods
end

target 'GulpsToday' do
  pod 'RealmSwift'
end

target 'GulpsTests' do
  common_pods
  pod 'Nimble', '~> 3.0.0'
  pod 'Quick', '~> 0.8.0'
  pod 'Nimble-Snapshots', '~> 3.0.0'
end

inhibit_all_warnings!
use_frameworks!

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['ENABLE_BITCODE'] = 'NO'
    end
  end
end
