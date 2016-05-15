# generate land code table

require 'json'
require 'fileutils'

LAND_CODE = {
  "10" => "宅地",
  "31" => "学校用地",
  "32" => "公園",
  "33" => "境内地",
  "34" => "墓地",
  "35" => "公衆用道路",
  "36" => "鉄道用地",
  "40" => "田",
  "50" => "畑",
  "60" => "牧場",
  "71" => "山林（保安林を除く。）",
  "72" => "保安林",
  "73" => "原野",
  "81" => "堤",
  "82" => "水道用地",
  "83" => "運河用地",
  "84" => "用悪水路",
  "85" => "井溝",
  "86" => "ため池",
  "87" => "池沼",
  "88" => "鉱泉地",
  "89" => "塩田",
  "90" => "雑種地",
}

def gen_land_json
  FileUtils.mkdir_p("api/v1")
  File.open("api/v1/jisx0411.json", "wb") do |f|
    f.write JSON.dump(LAND_CODE)
  end
end

task :default => :gen_json

desc "generate JSON file of Code for Categories of Land"
task :gen_json do
  gen_land_json
end
