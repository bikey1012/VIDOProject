# VIDOProject
VIDOProject
- Form 1: Quản Lý Sách.
CREATE TABLE [dbo].[SACH] (
	[MaSach] [char] (4) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL ,
	[TenSach] [nvarchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,
	[TacGia] [nvarchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,
	[MaTheLoai] [char] (4) COLLATE SQL_Latin1_General_CP1_CI_AS NULL ,
	[SoLuong] [int] NULL ,
	[DonGia] [money] NULL,
	[MaNXB] [char] (5) NULL
)
- Form 2: Quản Lý Menu.
CREATE TABLE [dbo].[MENU](
	[TEN_SAN_PHAM] [nvarchar](50) NULL,
	[LOAI] [nvarchar](50) NULL,
	[DON_VI_TINH] [nvarchar](50) NULL,
	[GIA_TIEN] [money] NULL
)
- Form 3: Quản Lý Nhà Cung Cấp.
CREATE TABLE [dbo].[NhaCungCap](
	[MaNCC] [varchar](50) NOT NULL,
	[TenNCC] [nvarchar](50) NULL,
	[DiaChi] [nvarchar](50) NULL,
	[SoDienThoai] [varchar](50) NULL,
	[ID] [int] IDENTITY(1,1) NOT NULL,
 CONSTRAINT [PK_NhaCungCap] PRIMARY KEY CLUSTERED 
(
	[ID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
- Form 4: Quản Lý Nhân Viên:
CREATE TABLE [dbo].[Nhan_Vien](
	[MA_NHAN_VIEN] [nvarchar](50) NOT NULL,
	[TEN_NHAN_VIEN] [nvarchar](50) NULL,
	[GIOI_TINH] [bit] NULL,
	[TUOI] [int] NULL,
	[MA_CHUC_VU] [nvarchar](50) NULL,
	[DIA_CHI] [nvarchar](50) NULL,
	[SDT] [int] NULL,
 CONSTRAINT [PK_Nhan_Vien] PRIMARY KEY CLUSTERED 
(
	[MA_NHAN_VIEN] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
) ON [PRIMARY]
