---
title: 'Home'
date: 2023-10-24
type: landing

design:
  # 1. 將全域間距從 6rem 加大到 8rem，增加呼吸感
  spacing: "8rem"

sections:
  # ---------------------------------------------------------
  # 第一區塊：Hero (主視覺)
  # ---------------------------------------------------------
  - block: hero
    content:
      title: Welcome to AE-LAB (Autonomous Edge LAB)
      # 2. 我在文字中間加了 HTML 的 <br> 標籤，強迫換行，避免文字擠成一坨
      text: |
        I am **Shengzhi Huang**, an Assistant Professor in the Department of Computer Science & Information Engineering at Tamkang University.<br><br>
        My research interests include **Edge AI**, **Multi-UAV Systems**, and **Financial Technology (FinTech)**.
      primary_action:
        text: View Publications
        url: /publication/
        icon: book-open
      secondary_action:
        text: Contact Me
        url: /#contact
    design:
      # 3. 增加 Hero 區塊上下的內部留白 (原本是 0)
      spacing:
        padding: ["2rem", 0, "4rem", 0]
      background:
        image:
          filename: "" 
          filters:
            brightness: 0.5

  # ---------------------------------------------------------
  # 第二區塊：Research Focus (這裡最容易覺得擠)
  # ---------------------------------------------------------
  - block: features
    id: research
    content:
      title: Research Focus
      text: My lab focuses on intelligent computing, autonomous systems, and quantitative financial analysis.
      items:
        - name: Edge AI & Optimization
          icon: cpu-chip
          description: Model quantization, compression, and deployment on embedded devices (NVIDIA Jetson / Raspberry Pi).
        - name: Multi-UAV Systems
          icon: paper-airplane
          description: Research on ad-hoc networks, dynamic role assignment, and energy-efficient path planning.
        - name: FinTech
          icon: chart-bar
          description: AI in stock market prediction, futures investment strategies, and global commodity tracking.
    design:
      css_class: "bg-gray-100 dark:bg-gray-800"
      columns: "3"
      # 4. 這裡將 padding 加大，讓這一塊跟上下拉開距離
      spacing:
        padding: ["5rem", 0, "5rem", 0]

# ---------------------------------------------------------
  # 第三區塊：最新動態 (Recent News)
  # ---------------------------------------------------------
  - block: collection
    content:
      title: Recent News
      text: ""
      filters:
        folders:
          - post
        exclude_featured: false
      count: 3
    design:
      # 這裡原本是 view: compact，請改成 view: card
      view: card
      # 這裡改成 3，變成橫向三欄，視覺上比較大氣
      columns: 3
---