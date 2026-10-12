# Introduction

For this project, I am configuring an HP EliteDesk 800 G3 with 500 GB of storage and an initial 8 GB of RAM, running Proxmox to enable experimentation with enterprise-level cybersecurity tools.

<!--
<mxfile host="app.diagrams.net">
  <diagram name="Page-1" id="SleDnQgNpbo-9ImH9l-U">
    <mxGraphModel grid="1" page="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" pageScale="1" pageWidth="850" pageHeight="1100" math="0" shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="66PR_tr1cIi5odt06scS-8" edge="1" parent="1" source="66PR_tr1cIi5odt06scS-1" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;entryX=0.5;entryY=0;entryDx=0;entryDy=0;endArrow=none;endFill=0;" target="66PR_tr1cIi5odt06scS-6">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-1" parent="1" style="rounded=0;whiteSpace=wrap;html=1;" value="Home Router" vertex="1">
          <mxGeometry height="60" width="120" x="350" y="170" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-3" edge="1" parent="1" source="66PR_tr1cIi5odt06scS-2" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;endArrow=none;endFill=0;" target="66PR_tr1cIi5odt06scS-1">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-2" parent="1" style="rounded=0;whiteSpace=wrap;html=1;" value="Internet" vertex="1">
          <mxGeometry height="60" width="120" x="350" y="20" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-5" edge="1" parent="1" source="66PR_tr1cIi5odt06scS-4" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;entryX=1;entryY=0.5;entryDx=0;entryDy=0;endArrow=none;endFill=0;" target="66PR_tr1cIi5odt06scS-1">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-4" parent="1" style="rounded=0;whiteSpace=wrap;html=1;" value="Home PC" vertex="1">
          <mxGeometry height="60" width="120" x="600" y="50" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-6" parent="1" style="rounded=0;whiteSpace=wrap;html=1;verticalAlign=top;" value="Server Running ProxMox" vertex="1">
          <mxGeometry height="30" width="550" x="135" y="260" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-9" edge="1" parent="1" source="66PR_tr1cIi5odt06scS-7" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;entryX=0.5;entryY=1;entryDx=0;entryDy=0;endArrow=none;endFill=0;" target="66PR_tr1cIi5odt06scS-6">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-7" parent="1" style="rounded=0;whiteSpace=wrap;html=1;" value="OPNSense Router" vertex="1">
          <mxGeometry height="60" width="120" x="350" y="490" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-10" parent="1" style="rounded=0;whiteSpace=wrap;html=1;labelPosition=left;verticalLabelPosition=top;align=right;verticalAlign=bottom;" value="" vertex="1">
          <mxGeometry height="300" width="550" x="135" y="290" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-11" parent="1" style="rounded=0;whiteSpace=wrap;html=1;labelBorderColor=none;strokeColor=none;fillColor=none;" value="Virtualised Environment" vertex="1">
          <mxGeometry height="60" width="120" x="120" y="290" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-14" edge="1" parent="1" source="66PR_tr1cIi5odt06scS-13" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;entryX=0.5;entryY=1;entryDx=0;entryDy=0;endArrow=none;endFill=0;" target="66PR_tr1cIi5odt06scS-6">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-13" parent="1" style="rounded=1;whiteSpace=wrap;html=1;" value="&lt;div&gt;OPNSense&lt;br&gt;Router&lt;/div&gt;" vertex="1">
          <mxGeometry height="60" width="120" x="350" y="320" as="geometry" />
        </mxCell>
        <mxCell id="LYBETa_LCv4HHzy-sqw2-6" edge="1" parent="1" source="66PR_tr1cIi5odt06scS-15" style="edgeStyle=orthogonalEdgeStyle;shape=connector;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;entryX=0;entryY=0.5;entryDx=0;entryDy=0;strokeColor=default;align=center;verticalAlign=middle;fontFamily=Helvetica;fontSize=11;fontColor=default;labelBackgroundColor=default;endArrow=none;endFill=0;" target="66PR_tr1cIi5odt06scS-13">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="66PR_tr1cIi5odt06scS-15" parent="1" style="rounded=1;whiteSpace=wrap;html=1;" value="&lt;div&gt;Ubuntu Splunk&lt;/div&gt;&lt;div&gt;Server&lt;/div&gt;" vertex="1">
          <mxGeometry height="60" width="120" x="160" y="350" as="geometry" />
        </mxCell>
        <mxCell id="LYBETa_LCv4HHzy-sqw2-7" edge="1" parent="1" source="LYBETa_LCv4HHzy-sqw2-2" style="edgeStyle=orthogonalEdgeStyle;shape=connector;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=default;align=center;verticalAlign=middle;fontFamily=Helvetica;fontSize=11;fontColor=default;labelBackgroundColor=default;endArrow=none;endFill=0;">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="300" y="380" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="LYBETa_LCv4HHzy-sqw2-2" parent="1" style="rounded=1;whiteSpace=wrap;html=1;fontFamily=Helvetica;fontSize=11;fontColor=default;labelBackgroundColor=default;" value="Vulnerable Windows Machine" vertex="1">
          <mxGeometry height="60" width="120" x="160" y="420" as="geometry" />
        </mxCell>
        <mxCell id="LYBETa_LCv4HHzy-sqw2-8" edge="1" parent="1" source="LYBETa_LCv4HHzy-sqw2-5" style="edgeStyle=orthogonalEdgeStyle;shape=connector;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=default;align=center;verticalAlign=middle;fontFamily=Helvetica;fontSize=11;fontColor=default;labelBackgroundColor=default;endArrow=none;endFill=0;">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="300" y="450" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="LYBETa_LCv4HHzy-sqw2-5" parent="1" style="rounded=1;whiteSpace=wrap;html=1;fontFamily=Helvetica;fontSize=11;fontColor=default;labelBackgroundColor=default;" value="Ubuntu Configuration Machine" vertex="1">
          <mxGeometry height="60" width="120" x="160" y="490" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
-->
# Table of Contents

1. [Hardware Setup, Research and deployment](Components%20of%20Setup/1.%20Hardware%20Setup,%20Research%20and%20deployment.md)
2. [Creation of Virtualised Router](Components%20of%20Setup/2.%20Creation%20of%20Virtualised%20Router.md)
3. [Setup of Log Generating Machine](Components%20of%20Setup/3.%20Setup%20of%20Log%20Generating%20Machine.md)
# Primary Objectives

1. Build a functioning Proxmox server
2. Familiarize with the inner operations of proxmox and virtualisation technology
3. Create a virtualised router
4. Create a virtual machine to house splunk
5. Create a vulnerable machine to generate logs for Splunk server